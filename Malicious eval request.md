> #### What is eval?
> 
eval() is a function available in multiple languages, that evaluates a string (can also be structured representation of code or some other special types according to the language) as an expression and returns a result.

<br>

> #### How can an eval function be malicious?
Using eval() with data from untrusted source may introduce secuity vulnerability, an attacker aware of the eval function use in a web site, application or a server can use it to exploit the vulnerability.
The eval function executes the code it is passed with the privillages of the caller, and if the code passed is affected by a malicious party, malicious code can end up running on a user machince or a server with the permission of the eval() caller, another concern is that a third party code accessing the scope in which eval was invoked can lead to possible attacks and not suspectable results.
In short, eval function can lead to code injection, allowing execution of arbitary code.

> #### Examples of resulting issues caused by injecting code in eval 
- User session hijacking
- Lead to DOM based XSS vulnerability
- Scrape user data
- Command injection attack

------
**Resources:**
- https://cobalt.io/blog/a-pentesters-guide-to-code-injection
- https://en.wikipedia.org/wiki/Eval
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/eval
- https://realpython.com/python-eval-function/
- https://owasp.org/www-community/attacks/Direct_Dynamic_Code_Evaluation_Eval%20Injection
