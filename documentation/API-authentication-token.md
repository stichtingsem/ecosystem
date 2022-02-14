# API authentication token

When requesting a token on the oauth2 token resource using the client_credentials a queryparameter containing the identifier for the school. A scope to access data can optionally be requested and if consent has been given, will be added as a scope in the token defined below.

Signed JWT with as minimum the following attributes:

client_id : identifier of application that has request this token (recipient)
scopes : list of scopes that client_id wants to access

The schoolid should be part of the token, but how is up to the idp and the api endpoint to agree how. The endpoint will need the ischoolid to verify for which schoolid the request or event is.

All this should be signed as described in the JWS specification.

An example of a token request could be: (to be discussed in https://github.com/stichtingsem/ecosystem/issues/43)

POST /token HTTP/1.1
Host: server.example.com
Content-Type: application/x-www-form-urlencoded

grant_type=client_credentials&client_id=[CLIENT_ID]&client_secret=[CLIENT_SECRET]&schoolid=[DIGI_DELIVERY_ID]
And if the token request was successful, the token response could be:

{
"access_token":"[ACCESS_TOKEN]",
"token_type":"Bearer",
"expires_in":86400,
}

## Validity of the token
The token will be valid for at least 30 minutes, more is up to the idp
