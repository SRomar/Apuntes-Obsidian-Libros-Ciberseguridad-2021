OSRF vulnerabilities **can exist even in situations where XSS is not possible.**

1. In every location where data submitted by one user is **displayed to other users ** but you cannot perform a stored XSS attack, review whether the application's behavior leaves it vulnerable to OSRF.
2. The vulnerability typically arises where user-supplied data is inserted into the target of a **hyperlink or other URL** within the returned page. Unless the application specifically blocks any characters you require,** it is almost certainly vulnerable**.
