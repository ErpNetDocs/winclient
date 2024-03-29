# Expression fields


Expression fields are user-defined fields that can be created in different forms in the database. With them, users can create calculated columns, which contain a value calculated from other columns or from the column values of multiple rows in the table. 

Аt first glance, еxpression fields and **[calculated attributes](xref:ca)**, which are introduced in Version 2017, have a similar purpose, but the calculated attributes are recommended for advanced users. Unlike them, expression fields can’t be used by **[user business rules](xref:ubr)**.
 
Like regular system fields, expression fields can be managed from the Customise fields form.

The expression fields have the following properties:

- **Field name** - the unique name of the expression fields; only latin letters and digits are accepted;
- **Caption** - the display name of the field; it is multi-language;
- **Expression** - numbers, symbols and operators or functions grouped together, which yields a new value by performing calculations, comparisons, or other operations;
- **Running total** - when activated, the sequence of numbers is summed and updated progressively, by adding the value of the new number to the previous running total;
- **Data type** - a format that contains the specific type of the value: boolean, integer, decimal, string, datetime or unset.

## Expressions
 
The term expression is synonymous with **formula**. In order to define an expression that needs to be evaluated in the system, we can use the **Expression editor**.

An expression consists of a number of possible elements that you can use, alone or in combination, to produce a result.

Those elements include:

- **Identifiers** - the names of table fields. In the editor, we can refer to a target field in the expressions by its ‘Field name’ surrounded by square brackets without spaces;
- **Operators** - such as + (plus) or - (minus). <br> For more information, see **[Expression fields - operators](operators.md)** ;
- **Functions** - such as IFF or ISNULL. <br> For more information, see **[Expression fields - functions](functions.md)**;
- **Constants**  - values that do not change, such as strings of text, or numbers that are not calculated by an expression.

