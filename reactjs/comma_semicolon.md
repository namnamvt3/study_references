#Semi-colon
## Automatic Semicolon Insertion (ASI) rules:
- A semicolon will be inserted when it comes across a line terminator or a '}' that is not grammatically correct. So, if parsing a new line of code right after the previous line of code still results in valid JavaScript, ASI will not be triggered.
    <br />
- If the program gets to the end of the input and there were no errors, but it's not a complete program, a semicolon will be added to the end. Which basically means a semicolon will be added at the end of the file if it's missing one.
    <br />
-  There are certain places in the grammar where, if a line break appears, it terminates the statement unconditionally and it will add a semicolon. One example of this is return statements.
##When Should I Not Use Semicolons?
if (...) {...} else {...}
for (...) {...}
while (...) {...}

## Note if do not use semi-colon
- If you're going to write your JavaScript without optional semicolons, it's probably good to at least know what ASI is doing. For example, compression or minification could cause your valid code to throw an error because those programs may rely on semicolons
<br />
- it can be harder to debug without semicolons since your code may be concatenating together without you realizing it. If you put a line break where there shouldn't be one, ASI may jump in and assume a semicolon even if there shouldn't be one.

# Semi-colon VS Comma
The comma operator is an operator that can be used inside an expression. It is used to separate out multiple different expressions and has the meaning "evaluate all of the following expressions, then produce the value of the final expression." For example:

a = 1, b = 2, c = 3
means "evaluate a = 1, then b = 2, then c = 3, then evaluate to the value of the expression c = 3.

The semicolon is not an operator and cannot be used inside an expression. It is used as part of JavaScript syntax to mark the end of an expression that is being treated as a statement. For example, you could say

a = 1; b = 2; c = 3;
And this would mean "there are three statements to do in sequence: evaluate the first expression as the first statement, the second expression as the second statement, and the third expression as the third statement."

In this regard, the two are not completely interchangeable. For example, you cannot write

var a = 1, var b = 2;
Because var a = 1 and var b = 2 are statements, not expressions, and thus can't be separated by commas. You would have to use a semicolon here.

(A note: you could say

var a = 1, b = 2;
because the language specifically permits this use of comma as a part of the syntax of a declaration statement. Here, comma is not used as an operator.)

Similarly, you can't say

a = (b = 1; c = 2);
Because here the right-hand side of the expression must be an expression, not a statement, and ; is used to separate statements. The inner semicolon would have to be a comma instead. (Then again, this code is pretty awkward and unusual in the first place, so you probably shouldn't do this at all!)

From a stylistic perspective, the comma operator is rarely used and is obscure enough that it might trip up reasonably competent JavaScript coders. As a result, I would strongly suggest not using it and instead following the established conventions in JavaScript about using semicolons to terminate statements, even if it would be equivalent and syntactically legal to use commas to separate out expressions that are each used as statements.