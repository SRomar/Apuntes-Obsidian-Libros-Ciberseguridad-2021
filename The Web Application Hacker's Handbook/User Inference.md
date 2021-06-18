1. Differences in the timing of the application responses may be subtle and difficult to detect. In a typical situation, it is worth probing the application for this behavior only in selected key areas where a crucial item of interesting data is submitted and where the kind of processing being performed is likely to result in time differences.
2. To test a particular function, **compile one list containing several items that are known to be valid** (or that have been accessed recently) and a **second list containing items that are know to be invalid** (or dormant). Make only one request at a time, and monitoring the **time taken for the application to respond to each request**. Determine whether there is any correlation between the item's status and the time taken to respond.
3. **You can use Burp Intruder to automate this task. **For every request it generates, intruder automatically records the time taken before the application responds and the time taken to complete the response. Yo can sort a table of results by either of these attributes to quickly identify any obvious correlations