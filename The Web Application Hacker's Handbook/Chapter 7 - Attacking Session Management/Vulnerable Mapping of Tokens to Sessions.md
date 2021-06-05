Permitting concurrent sessions is undesirable, because it allows users to persist in undesirable practices without inconvenience and because it allow an attacker to use captured credentials without risk of detection.

2. Log in and log out several times using the same user account, either from different browser processes or from different computers. Determine whether a new session token is issued each time or whether the same token is issued each time you log in. If the latter occurs, the application is not really employing proper sessions.
