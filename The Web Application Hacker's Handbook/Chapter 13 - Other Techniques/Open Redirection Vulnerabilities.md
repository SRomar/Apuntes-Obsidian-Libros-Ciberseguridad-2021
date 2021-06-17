[Open redirection (reflected)](https://portswigger.net/kb/issues/00500100_open-redirection-reflected#:~:text=Open%20redirection%20vulnerabilities%20arise%20when,to%20an%20arbitrary%20external%20domain)

[Using Burp to Test for Open Redirections](https://portswigger.net/support/using-burp-to-test-for-open-redirections)

1. Identify every instance within application where a redirect occurs.
2. An effective way to do this to walk through the application using an intercepting proxy and monitor the requests made for actual pages (as opposed to other resources, such as images, stylesheets, and scripts)
3. If a single navigation action results in more than one request in succession, investigate what means of performing the redirect is being used.
4. If the user data being processed in a redirect contains an absolute URL, modify the domain name within the URL, and test whether the application redirects you to the different domain.
5. If the user data being processed contains a relative URL, modify this into an absolute URL for a different domain, and test whether the application redirects you to this domain.
