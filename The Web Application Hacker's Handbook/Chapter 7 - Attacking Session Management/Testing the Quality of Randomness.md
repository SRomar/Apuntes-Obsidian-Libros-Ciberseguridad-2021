The high-level steps in this process are as follows:

1. Start with the hypothesis that the tokens are randomly generated.
2. Apply a series of tests, each of which observers specific properties of the sample that are likely to have certain characteristics if the tokens are randomly generated.
3. ** For each test, calculate the probability of the observed characteristics occurring, working on the assumption that the hypothesis is true.**
4. If this probability falls below a certain level (the "significance level"), reject the hypothesis and conclude that the tokens are not randomly generated.


Keep in mind two important caveats when performing statistical test for randomness. These caveats affect the correct interpretation of the test results and their consequences for the application's security posture. First, **tokes that are generated in a completely deterministic way may pass the statistical test for randomness. **For example, a linear congruential pseudorandom number generator, or an algorithm that computes the hash of a sequential number, may produce output that passes the test. Yet an attacker who knows the algorithm and the internal state of the generator can extrapolate its output with complete reliability in both forward and reverse  directions. 

Second, **tokens that fail the statistical test for randomness may not actually be predictable in any *practical* situation**. If a given bit of a token fails the tests, this means only that the sequence of bits observed at that position contains characteristics that are unlikely to occur in a genuinely random token. But attempting to predict the value of that bit in the next token, based on the observed characteristics, may be little more reliable than blind guesswork. Multiplying this unreliability across a large number of bits that need to be predicted simultaneously may mean that the probability of making a correct prediction is extremely low.




