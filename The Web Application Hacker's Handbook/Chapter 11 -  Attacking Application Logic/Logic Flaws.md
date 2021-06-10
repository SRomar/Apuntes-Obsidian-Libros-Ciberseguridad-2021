1. Try **removing in turn each parameter submitted in requests, including cookies, query string fields, and items of POST data.**
2. Be sure to **delete the actual name of the parameter** as well as its value. Do not just submit any empty string, because typically the server handles this differently.
3. Attack only **one parameter at a time** to ensure that all relevant code paths within the application are reached.
4. If the request you are manipulating is part of a multistage process, **follow the process through to completion**, because some later logic may process data that was supplied in earlier steps and stored within the session.
5. 
