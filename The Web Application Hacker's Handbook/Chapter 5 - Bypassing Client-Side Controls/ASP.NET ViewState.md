**Verify if MAC protection is enabled**. If you are using Burp Scanner with passive scanning enabled, Burp automatically reports any pages that use the ViewState without MAC protection.

Is a hidden field that is created by default in all [[ASP.NET]] web applications. It contains **serialized information about state of the current page**. 

The ViewState parameter is actually a Base64-encoded string that can be easily decoded to see the price parameter that has been placed there,