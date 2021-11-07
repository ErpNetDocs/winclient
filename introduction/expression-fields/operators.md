# Operators


Every expression consists of at least one operand and can have one or more operators. Operands are values, whereas operators are symbols that represent particular actions. 

## When we create comparison expressions, the following operators are allowed

### '<' - Less than operator

Returns True if the left operand is less than the right operand.

***Example***:        3 < 4 // true



### '>' - Greater than operator

Returns True if the left operand is greater than the right operand.

***Example***:        4 > 3 // true



### '<=' - Less than or equal to operator

Returns True if the left operand is less than or equal to the right operand.

***Example***:        3 <= 4 // true <br>
3 <= 3 // true



### '>=' - Greater than or equal operator

Returns True if the left operand is greater than or equal to the right operand.

***Example***:         4 >= 3 // true <br>
3 >= 3 // true



### '<>' – Inequality operator

Returns True if the operands do not have the same value; otherwise, it returns False.

***Example***:         4 <> 3   // true



### '=' – Equality operator

Returns True if both operands have the same value; otherwise, it returns False.

***Example***: 3 = 3   // true



### In(,,,) - IN operator

Tests if the column value is equal to any one of a specified set of values. It is useful when you want to compare a column with more than one value. It is similar to an OR condition.

**Syntax:** *expression* In (*value1, value2,* …), where:

           - *expression* - expression identifying the field that contains the data you want to evaluate;
           - *value1, value2* - *expression* or list of expressions against which you want to evaluate the *expression*.

If the *expression* is found in the list of values, the In operator returns True; otherwise, it returns False.

> [!NOTE]
> 
> If we are using characters or dates list items, they must be enclosed in single quotation marks ('').

***Example:*** [Quantity]In(1, 2, 5 )

The operator will return True for the rows where the quantity is either of '1', ‘2’ or ‘5’; otherwise, it returns False.



### Like() - LIKE operator

Tests if the column value is similar to specified character(s). The LIKE operator is used to list all rows in a table whose column values match a specified pattern. It is useful when you want to search rows to match a specific pattern, or when you do not know the entire value.

***Syntax:*** *expression* Like ('*pattern*'), where: 

         - *expression* - expression identifying the field that contains the data you want to evaluate;
         - *pattern* - string or character string literal against which *expression* is compared.

> [!NOTE]
> 
> If we are using characters or dates list items, they must be enclosed in single quotation marks (‘).

The following table shows how you can use **Like** to test expressions for different patterns.

|Kind of match|Pattern|Match(returns True)|No match(returns False)
|:----|:----|:----|:---
|Multiple character|a*a|aa, Aba, aBBBa|Abc
| |*ab*|abc|AABB|Xab|aZb, bac
|Special character|a[*]a|a*a|aaa
|Multiple characters|ab*|abcdefg, abc|cab, aab
|Single character|a?a|aaa, a3a, aBa|aBBBa
|Single digit|a#a|a0a, a1a, a2a|aaa, a10a
|Range of characters|[a-z]|f, p, i|2, &
|Outside a range|[!a-z]|9,&,%|b, a
|Not a digit|[!0-9]|A. a. &, ~|0, 1, 9
|Combined|a[!B-M]#|An9,az0, a99|abc, aj0

- **Concatenation** is allowed using Boolean AND, OR, and NOT operators. The AND operator has precedence over other operators. 
 
***For example***:
  
  (LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John'

To concatenate a string, use the + character.

The following arithmetic operators are also supported in expressions:

- "+ **(addition)**" - Adds the value of one numeric expression to another, or concatenates two strings.
- "- **(subtraction)**" - Finds the difference between two numbers.
- "* **(multiplication)**" - Multiplies the value of two expressions.
- "/ **(division)**" - Divides the first operand by the second.
- "% **(modulus)**" - Returns the remainder (modulus) obtained by dividing one numeric expression into another.

