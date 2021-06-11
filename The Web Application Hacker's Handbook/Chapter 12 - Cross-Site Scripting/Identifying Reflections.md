1. If you identify XSS-like behavior in a request that contains nonstandard content, the first thing you should do is quickly **verify whether the behavior remains when you change the *Content-Type* header to *text/plain*.** If it does not, it may be worth investing any further effort in trying to develop a working XSS exploit.
2.  **Choose a unique arbitrary string** that does not appear anywhere within the application and that contains only alphabetical characters and therefore is unlikely to be affected by any XSS-specific filters For example:
			dondeestanlospibesqueahoragritanelmccacoaguante

	**Submit this string as every parameter to every page**, targeting only one parameter at a time.
2. Make a note of every parameter whose value is being copied into the application's response. **These are not necessarily vulnerable**, but each instance identified is a candidate for further investigation. Each appearance of the string may be subject to different protective filters and therefore needs to be investigated separately.
3. In any cases where XSS was found in a POST request, use the "change request method" option in Burp to determine whether the same attack could be performed as GET request. 
4. You should test every instance in which the application processes the contents of an HTTP request header.** A common XSS vulnerability arises in error messages**, where items such as the **[[Referer Header]]** and User-Agent headers are copied into the message's contents. These headers are valid vehicles for delivering a reflected XSS attack.
5. Test your exploit by submitting it to the application. **If your crafted string is still returned unmodified, the application is vulnerable**. 
6. Often, when you are trying to fine-tune an attack in an unusual situation, it can be helpful to **view the virtual HTML **that the browser constructs out of the server's actual response.

 