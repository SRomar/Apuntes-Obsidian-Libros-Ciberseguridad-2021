The HTTP protocol includes its own mechanisms for authenticating users using various authentication schemes, including the following:

Example: `WWW-Authenticate: Basic realm="User Visible Realm"`


-	**Basic**:  is a simple authentication mechanism that sends user credentials as a Base64-encoded string in a request header with each message.
-	**NTLM**: is a challenge-response mechanism and uses a version of the Windows NTLM protocol.
-	**Digest**: is a challenge-response mechanism and uses [[MD5]] checksums of a nonce with the users's credentials.