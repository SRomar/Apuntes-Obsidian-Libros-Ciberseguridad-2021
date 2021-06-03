# Cookies 

Unlike the other types of request parameters, cookies continues to be **resubmitted in each subsequent request** without any particular action required by application or the user.


[[Set-Cookie]] header: 
- **expires**: sets date until which the cookie is valid. This causes the browser to save the cookies to persistent storage, and **it is reused in subsequent browser sessions until the expiration date is reached.**

- **domain**: specifies the domain for which the cookie is valid. This must be **the same or a parent of the domain** from which the cookies is received.

- **path**: specifies the URL path for which the cookies is valid.

-  **secure**: If this attribute is set, the cookies will be submitted **only in HTTPS**.
-
-  **HttpOnly**: If this attribute is set, the cookie **cannot be directly accessed via client-side JavaScript.** 

