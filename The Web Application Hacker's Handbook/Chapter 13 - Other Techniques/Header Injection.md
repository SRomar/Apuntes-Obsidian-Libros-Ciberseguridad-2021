https://portswigger.net/web-security/host-header

1. For each potentially vulnerable instance in which **user-controllable input is copied into an HTTP header**, verify whether the application accepts data containing URL-encoded carriage-return(**%0d**) and line-feed(**%0a**) characters, and whether these are returned **unsanitized** in its response.
2. Note that you are **looking for the actual newline** characters themselves to appear in the server's response, **not their URL-encoded equivalents.** If you view the response in an intercepting proxy, you should see an additional line in the HTTP headers if the attack was successful.
3. If only one of the two newline characters is returned in the server's responses, it may still be possible to craft a working exploit, depending on the context.
4. Ensure that you are reading the HTTP response headers using an intercepting proxy tool.
5. 