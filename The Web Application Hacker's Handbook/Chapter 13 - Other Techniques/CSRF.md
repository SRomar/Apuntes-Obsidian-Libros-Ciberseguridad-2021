The attacker creates an innocuous looking website that causes the **user's browser to submit a request directly to the vulnerable application** to perform some unintended action that is beneficial to the attacker.

CSRF vulnerabilities arise primarily in cases where **applications rely solely on HTTP cookies for tracking sessions. ** Once an application has set a cookie in a user's browser, the browser automatically submits that cookie to the application in every subsequent request. This is true **regardless of whether the request originates from** a link, form within the application itself, or from other source such as an external website or a link clicked in an e-mail. If the application does not take precautions against an attacker's "riding" on its users' sessions in this way, it is vulnerable to CSRF.

3. Create an HTML page that issues the desired request without any user interaction. For GET requests, you can place *img* tag with the *src* attribute  set to the vulnerable URL. For POST requests, you can create form that contains hidden fields for all the relevant parameters required for the attack and that has its target set to the vulnerable URL. You can use JavaScript to autosubmit the form as soon as the page loads.


