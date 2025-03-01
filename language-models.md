# Language Models

Input: String of words or text
Output: Probability that this string could appear in a given language

Many, many parameters with huge inputs

Large amounts of data are fed to the model and it creates a probability distribution that we can sample from to output a sentence.

## Auto-Regressive vs Regressive Models


**Autoregressive:** Prediction based on past observations. Depends on itself (auto). x(t) <- response = f(x(t-1), x(t-2) ...) <- regressors

**Regressive:** Depends on other signals /data; weighted sum of these other functions. x(t) = B1 a(t) + B2 b(t) ...
    - Encoder/decoder