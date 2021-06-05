1. If HTTP authentication is being used, it is possible that no session management mechanism is implemented.
2. Sessionless indicators:
	1. Token-like data items issued to the client are fairly long (100 or more bytes)
	2. The application issues a new token-line item in response to every request.
	3. The data in the item appears to be encrypted (and therefore has no discernible structure) or signed (and therefore has a meaningful structure accompanied by a few bytes of meaningless binary data).
