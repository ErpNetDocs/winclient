# Functions


Functions can be used in formulas to perform simple or complex calculations. You can create a formula with a function that obtains its argument from the result of another function.

## The following functions are supported

### CONVERT()

Converts an expression of one data type to another. 

This function is very useful if we want to use custom properties values in calculations. We can use all data types which are available in the dropdown list in the **Expression fields** editor. Data types must be used in the following format 'System.DataType' - they have to be preceded by 'System' and have to be enclosed in single quotation marks ('').

> [!NOTE]
> 
> All conversions are valid with the following exceptions:<br> **Boolean** can be converted to and from **integer**, **string** and itself only. <br>
**DateTime** can be converted to and from **string** and itself only. 

***Syntax:*** Convert (expression, type), where:

-expression - The expression to convert.

***Example:*** CONVERT([LinesTotal], 'System.Decimal').  

### LEN()

Gets the length of a string.

***Syntax***: LEN(*expression*), where:

-expression - The string to be evaluated.

***Example:*** Len([ProductDescription]) 

If the product description is ‘White paper’, the function will return 11.

### ISNULL()

Checks an expression and either returns it or gives a replacement value.

***Syntax:*** ISNULL(expression, replacementvalue), where:

-expression - The expression to check.
-replacementvalue - If expression is null, a replacement value is returned.

***Example:*** IsNull([UnitPrice], 0.00)

If the unit price is 12.00, then the function returns 12.00. If the unit price is not filled in, it returns 0.00.

### IIF()

Gets one of two values depending on the result of a logical expression.

***Syntax:*** IIF(expr, truepart, falsepart), where:

-expr - The expression to evaluate.
-truepart - The value to return if the expression is true.
-falsepart - The value to return if the expression is false.
 
 ***Example:*** IIF([LineAmount]>1000, 'Eligible for discount', 'No discount')
 
If the Line amount is 2000.00, the function returns ‘Eligible for discount’.

If the Line amount is 800.00, the function returns ‘No discount’.

### TRIM()

Removes all leading and trailing blank characters.

***Syntax:*** TRIM(expression), where:

-expression - The expression that will be trimmed.

***Example:*** TRIM([Notes])

If the note is ‘The warranty is sold separately. ‘, the function will return ‘The warranty is sold separately.’.

### SUBSTRING()

Gets a sub-string of a specified length, starting at a specified point in the string.

***Syntax:*** SUBSTRING(expression, start, length), where:

-expression - The source string for the substring.</br>
-start - An integer that defines where the substring starts.</br>
-length - An integer that defines the length of the substring.</br>
 
 ***Example:*** SUBSTRING([ProductDescription], 7, 5)
 
If the Product description is ‘White paper’, then the function will return ‘Paper’.

