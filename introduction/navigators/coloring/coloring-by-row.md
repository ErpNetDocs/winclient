# Conditional coloring by row

This procedure will show you how to view the rows of overdue payments in color (for any navigator). 

As an example, we will set all payments, overdue for more than 30 days, to show up in red. For that purpose, you can first open the respective navigator: 

<b>Main Menu -> Finance -> Payments -> Payments Status</b>

The <b>Payments Status</b> navigator shows the payments due to/from our contractors - customers and suppliers.

1.	Click on <b>Show Data</b> and then right-click on the rows of the navigator. From the displayed menu select **Customize fields**; 
2.	The <b>Customize fields</b> window will open, then you need to click on the <b>Expression Format Conditions</b> button: 

![Customize fields](pictures/customize-fileds.png)
 
A window will open for you to enter the desired conditions:

![Format Conditions](pictures/format-conditions.png)

3.	Click on <b>Add</b> to open a new window. Here, select the Fields option. In the small middle section you will see all fields that you can use to set conditional coloring for:

![Condition expression editor](pictures/condition-expression-editor.png)
 
As an example, we will set all payments, overdue for more then 30 days, to light up in red. For that purpose, double click on the <b>'Overdue Days'</b> field (it will be added to the expression at the top of the window). Then manually type in '> 30' (the greater-than sign and the number 30 without the quotes) after [Overdue Days].

Click on the <b>'OK'</b> button

![Overdue Days](pictures/overdue-days.png)

4.	After you set the condition, you need to choose a color:

![Selecting color](pictures/select-color.png)

5.	With that, the program will color all the rows with payments, overdue for more than 30 days, in red:

![Colored lines](pictures/colored-rows.png)
