# API authentication token

When requesting a token on the oauth2 token resource using the client_credentials a queryparameter containing the identifier for the school. A scope to access data can optionally be requested and if consent has been given, will be added as a scope in the token defined below.

Signed JWT with as minimum the following attributes:

client_id : identifier of application that has request this token (recipient)
scopes : list of scopes that client_id wants to access

optional (proposal):
schoolidentifier: requested digideliveryid 
parentidentifier: digideliveryid of parent organisation

All this should be signed as described in the JWS specification.

## Validity of the token
The token will be valid for at least 30 minutes
