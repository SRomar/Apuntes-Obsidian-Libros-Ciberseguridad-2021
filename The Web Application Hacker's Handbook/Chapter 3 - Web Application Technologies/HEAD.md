HEAD method is not considered dangerous but it can be used to attack a web application by **mimicking the GET request**. For example, the default security constraint of JAVA EE web.xml files restricts only the GET and POST methods, so the HEAD request can be sent to the target URL to initiate the execution to bypass the authentication.