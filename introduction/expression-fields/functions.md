# Functions


Functions can be used in formulas to perform simple or complex calculations. You can create a formula with a function that obtains its argument from the result of another functions.
## The following functions are supported:

- ### CONVERT()
Converts an expression of one data type to another. This function is very useful if we want to use custom properties values in calculations. We can use all data types which are available in the drop down list in the Expression fields editor. Data types must be used in the following format 'System.DataType' - they have to be preceded by System and have to be enclosed in single quotation marks ('').

>[**!Note:]**  All conversions are valid with the following exceptions: **Boolean** can be converted to and from **Integer**, **String** and itself only. **DateTime** can be converted to and from **String** and itself only. 

***Syntax:*** Convert (expression, type), where:
*-expression* - The expression to convert.

***Example:*** CONVERT([LinesTotal], 'System.Decimal').  

- ### LEN()
Gets the length of a string.

***Syntax***: LEN(*expression*), where:</br> 
-expression - The string to be evaluated.

***Example:*** Len([ProductDescription]) </br>
If the product description is ‘White paper’, the function will return 11.
- ### ISNULL()

Checks an expression and either returns the checked expression or a replacement value.

***Syntax:*** ISNULL(expression, replacementvalue), where:</br>
-expression - The expression to check.</br>
-replacementvalue - If expression is null, replacementvalue is returned.

***Example:*** IsNull([UnitPrice], 0.00)</br>
If the Unit price is 12.00, then the function returns 12.00. If the Unit price is not filled in, then returns 0.00.

- ### IIF()

Gets one of two values depending on the result of a logical expression.

***Syntax:*** IIF(expr, truepart, falsepart), where:</br>
-expr - The expression to evaluate.</br>
-truepart - The value to return if the expression is true.</br>
-falsepart - The value to return if the expression is false.</br>
 
 ***Example:*** IIF([LineAmount]>1000, 'Eligible for discount', 'No discount')</br>
If the Line amount is 2000.00, the function returns ‘Eligible for discount’.</br>
If the Line amount is 800.00, the function returns ‘No discount’.
- ### TRIM()

Removes all leading and trailing blank characters.

***Syntax:*** TRIM(expression), where:</br>
-expression - The expression to trim.</br>

***Example:*** TRIM([Notes])</br>
If the note is ‘The warranty is sold separately. ‘, then the function will return ‘The warranty is sold separately.’.

- ### SUBSTRING()

Gets a sub-string of a specified length, starting at a specified point in the string.

***Syntax:*** SUBSTRING(expression, start, length), where:</br>
-expression - The source string for the substring.</br>
-start - Integer that specifies where the substring starts.</br>
-length - Integer that specifies the length of the substring.</br>
 
 ***Example:*** SUBSTRING([ProductDescription], 7, 5)’</br>
If the Product description is ‘White paper’, then the function will return ‘Paper’.

