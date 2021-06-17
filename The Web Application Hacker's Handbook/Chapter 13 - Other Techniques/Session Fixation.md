https://secureteam.co.uk/articles/web-application-security-articles/understanding-session-fixation-attacks/

https://www.acunetix.com/blog/web-security-zone/what-is-session-fixation/

https://www.youtube.com/watch?v=tkSmaMlSQ9E

**If the application supports authentication**, you should review how it handles session tokens in relation to the login. The application may be vulnerable in two ways:

- The application issues an anonymous session token to each unauthenticated user. When the user logs in, **no new token is issued**. Instead, he existing session is upgraded to an authenticated session. This behavior is common when the application uses the application server's default session-handling mechanism.
- The application does** not issue tokens to anonymous users**, and a token is issued only following a successful login. However, if a user accesses the login function using an authenticated token and logs in using different credentials, no new token is issued. Instead, the user associated with the previously authenticated session is changed to the identity of the second user.

In both of these cases, an attacker can obtain a valid session token and feed this to a target user.

1. **Obtain a valid token** whatever means the application enables you to obtain one.
2. Access the login form, and perform a** login using this token.**
3. If the login is successful the application does not issue a new token, **it is vulnerable to session fixation.**

Session fixation vulnerabilities **can also exist in applications that do not contain login functionality**. For example, an application may allow anonymous users to browse a catalog of products, place items into a shopping cart, check out by submitting personal data and payment details, and then review all this information on a Confirm Order page. In this situation, an attacker may fix an anonymous session token with a victim's browser, wait for that user to place an order and submit sensitive information, and then access the confirm order page using the token to capture the user's details.

If the application does not support authentication but does allow user to submit and the review sensitive information, **you should verify whether the same session token is used before and after the initial submission of user-specific information.** If it is, an attacker can obtain a token and feed it to a target user. When the user submits sensitive details, the attacker can use the token to view the user's information.

1. **Obtain a session token as a completely anonymous user**, and then walk through the process of submitting sensitive data, up until any page at which the sensitive data is displayed back. 
2. If the same token originally obtained can now be used to retrieve the sensitive data, the application is vulnerable to session fixation.
3. If any type of session fixation is identified, verify whether the **server accepts arbitrary tokens** it has not previously issued. If it does, the vulnerability is considerably easier to exploit.







