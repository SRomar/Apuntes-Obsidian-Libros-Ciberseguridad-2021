[[ECB Ciphers]]
[[CBC Ciphers]]
 
 
** Some applications use the technique of encrypting meaningful data within request parameters more generally in an attempt to prevent tampering of data**, such as the prices of shopping items. In any location where you see apparently encrypted data that plays a key role in application functionality, you should try the bit-flipping technique to see whether you can manipulate the encrypted information in a meaningful way to interfere with application logic.

To prevent various attacks that manipulate file paths, an application encrypted the file within this parameter. However, if a user requested a file that had been deleted, the application displayed an error message showing the **decrypted** name of the requested file.