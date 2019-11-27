# Semi-colon
## Automatic Semicolon Insertion (ASI) rules:
- A semicolon will be inserted when it comes across a line terminator or a '}' that is not grammatically correct. So, if parsing a new line of code right after the previous line of code still results in valid JavaScript, ASI will not be triggered.
    <br />
- If the program gets to the end of the input and there were no errors, but it's not a complete program, a semicolon will be added to the end. Which basically means a semicolon will be added at the end of the file if it's missing one.
    <br />
-  There are certain places in the grammar where, if a line break appears, it terminates the statement unconditionally and it will add a semicolon. One example of this is return statements.
## When Should I Not Use Semicolons?
if (...) {...} else {...}
for (...) {...}
while (...) {...}

## Note if do not use semi-colon
- If you're going to write your JavaScript without optional semicolons, it's probably good to at least know what ASI is doing. For example, compression or minification could cause your valid code to throw an error because those programs may rely on semicolons
<br />
- it can be harder to debug without semicolons since your code may be concatenating together without you realizing it. If you put a line break where there shouldn't be one, ASI may jump in and assume a semicolon even if there shouldn't be one.

# Semi-colon VS Comma
- **The comma operator** is an operator, used inside an expression to separate out multiple different expressions. 
For example:
a = 1, b = 2, c = 3
<br />
- The semicolon is not an operator and cannot be used inside an expression. It is used as part of JavaScript syntax to mark the end of an expression that is being treated as a statement. 
For example:
a = 1; b = 2; c = 3;
mean "there are three statements to do in sequence