Instructs the browser to use its cached copy of the requested resource.

When this occurs, and you need to** intercept and modify the resource that the browser has cached**, you can intercept the relevant request and **remove the *If-Modified-Since* and *If-None-Match*** headers. This causes the server to respond with the full version of the requested resource.