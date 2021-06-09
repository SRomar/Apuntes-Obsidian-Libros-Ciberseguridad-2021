It involves circumventing any controls imposed by in-browser navigation on the sequence in which application functions may be accessed:

1. Attempt to submit these ** request out of the expected sequence**. Try skipping certain stages, accessing a single stage more than once, and accessing earlier stages after later ones.
2.  The sequence of stages may be accessed via series of GET or POST requests for distinct URLs, or they may involve submitting different  sets of parameters to the same URL. The stage being requested may be specified by submitting a function name or index within a request parameter. 
3.  **Take parameters that are submitted at one stage of the process and try submitting these to a different stage.** 