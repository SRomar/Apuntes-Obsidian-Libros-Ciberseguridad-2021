DOM-based XSS bugs may exists in any location where client-side scripts are used, regardless of the type of page or whether you see parameters being submitted to the page. 

**In every instance where one of the preceding APIs is being used**, closely review the code to identify what is being done with the user-controllable data, and whether crafted input could be used to cause execution of arbitrary JavaScript. In particular, review and test any instance where your data is being passed to any of the following APIs.

https://portswigger.net/web-security/cross-site-scripting/dom-based