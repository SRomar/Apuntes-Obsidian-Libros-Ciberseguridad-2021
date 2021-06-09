1. You can normally **use the ping command as a means of triggering a time delay** by causing the server to ping its loopback interface for specific period. There are minor differences between how Windows and UNIX-based platforms handle command separator and the ping command. However, the following all-purpose test string should induce a 30-second time delay on either platform if no filtering.
	
	|| ping -i 30 127.0.0.1 ; x || ping -n 30 127.0.0.1 &
	
	To maximize your chances of detecting a command injection flaw if the application is filtering certain command separators, you should also submit each of the following test string to each targeted parameter in turn and monitor the time taken for the application to respond:
	
	| ping -i 30 127.0.0.1 | 
	| ping -n 30 127.0.0.1 |
	& ping -i 30 127.0.0.1 &
	; ping 127.0.0.1;
	%0a ping -i 30 127.0.0.1 %0a
	`ping 127.0.0.1` 
	
2. If a time delay occurs, the application may be vulnerable to command injection. Repeat the test case several times to confirm that the delay was not the results of network latency or other anomalies. You can try changing  the value of the -n or  -i parameters and confirming that the delay experienced varies systematically with the value supplied.
4. If you are unable to retrieve results directly, you have other options:
	1.   You can attempt to open out-of-band channel back to your computer. Try using [[TFTP]] to copy tools up to the server, using [[telnet]] or [[netcat]] to create a reverse shell back to your computer, and using the mail command to send command output via [[SMTP]].
	2.   You can redirect the results of your commands to a file within the web root, which you can then retrieve directly using your browser. For example:
			dir> c:\inetpub\wwwroot\foo.txt
		