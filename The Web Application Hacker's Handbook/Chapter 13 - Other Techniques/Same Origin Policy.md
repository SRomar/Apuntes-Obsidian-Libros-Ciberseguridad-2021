
You should always check for the **[/crossdomain.xml](https://cwe.mitre.org/data/definitions/942.html)** file on any web application you are testing. Even if the application itself does not use Flash, if permission is granted to another domain, Flash objects issued by that domain are permitted to interact with the domain that publishes the policy.

- If the application allows unrestricted access, any other site can perform two-way interaction, riding on the sessions of application users.
- Some policy files disclose intranet hostnames or other sensitive information that may be of use to an attacker.

#### HTML5
[XMLHttpRequest](https://www.paladion.net/blogs/xmlhttprequest-based-csrf-test-1-0-part-1)(XHR) allows request to be issued only to the same origin as the invoking page. With HTML5, this technology is being modified to allow two-way interaction with other domains, provided that the domains being accessed give permission.

1. To test an application's handling of cross-domain requests using XHR, you should **try adding an *Origin* header specifying a different domain**, and examine any *Access-Control * headers that re returned. The security implications of allowing two-way access from any domain, or from specified other domains are the same as those described for the Flash cross-domain policy.
2. If any cross-domain access is supported, you should also **use *OPTIONS* requests to understand exactly what headers and other requests details are permitted.**

**If cross-domain access is denied by the targeted application**, it is necessary to increment a value in a URL parameter to ensure that each request is for a different URL and therefore is actually issued by the browser.

