# API authentication token

For communication between the parties an authentication token is used that contains the identity of the party and sometimes the identity of the school on which behalve of the party communicates
For example the SIS sends events on behalve of a school to the LMS. For each school a new token is required. Requesting a catalogue by the MP from a LA will only need a token with the identity of the MP, as the MP does not request it in the context of a school.
Next to the identities a scope to access data can optionally be requested and if consent has been given, will be added as a scope in the token defined below. In this way a token can only be used for the API it is intended and which the school has given consent.

The way a token will be requested will be part of the specification here. A token will be requested with OAuth2 client_credentials flow using one optional (only when requesting in school context) custom queryparameter. The name of this queryparameter is `schoolidentifier` and currently contains the digideliveryid of the school. 
The token given out will be used for the context API call with context of this school. 

The format of the content of the access_token is not part of the standard but just a recommendation on how to save schoolcontext to a token, which then can be used in your backend system to check actual permissions for this context. We recommend the bearer access_token to be a Signed JWT with at least the following properties:

* jti = unique identifier for this token
* aud = audience, client_id of the oauthclient that requested the token
* scope = scope available for this oauthclient
* iss = issuer, identifier of the idp, mostly base url
* schoolidentifier = digideliveryid requested (and validated by the idp for existence) (Note: this was in previous examples schoolid ! This might have caused confusion)

More properties can be added as needed by the idp for correct handling of client's authorisation. (recommended to add `exp` for expiry, `iat` of moment of issue).

Adding all these properties allow us to validate a token with the public key of the idp, potentially without doing a database roundtrip. In the API resources the schoolidentifier can be consumed from the token and used to calculate the permissions available for this school in the API.

An example of a token request could be:
POST /token HTTP/1.1
Host: server.example.com
Content-Type: application/x-www-form-urlencoded

grant_type=client_credentials&client_id=[CLIENT_ID]&client_secret=[CLIENT_SECRET]&schoolid=[DIGI_DELIVERY_ID]&schoolidentifier=[DIGI_DELIVERY_ID]
And if the token request was successful, the token response could be:

{
"access_token":"[ACCESS_TOKEN]",
"token_type":"Bearer",
"expires_in":86400,
}

Validity of the token
The token will be valid for at least 30 minutes, more is up to the idp
A token is only valid for one school identity. when a saas application wants to send information on behalf of a different school a new token should be requested.
Tokens can be cached until expired.
