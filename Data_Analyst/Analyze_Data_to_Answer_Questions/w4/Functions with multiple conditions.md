Functions with multiple conditions
----------------------------------

In this reading, you will learn more about conditional functions and how to construct functions with multiple conditions. Recall that conditional functions and formulas perform calculations according to specific conditions. Previously, you learned how to use functions like SUMIF and COUNTIF that have one condition. You can use the SUMIFS and COUNTIFS functions if you have two or more conditions. You will learn their basic syntax in Google Sheets, and check out an example.

Refer to the resources at the end of this reading for information about similar functions in Microsoft Excel.

### SUMIF to SUMIFS

The basic syntax of a SUMIF function is: =SUMIF(range, criterion, sum_range)

The first range is where the function will search for the condition that you have set. The criterion is the condition you are applying and the sum_range is the range of cells that will be included in the calculation.

For example, you might have a table with a list of expenses, their cost, and the date they occurred.


You could use SUMIF to calculate the total price of fuel in this table, like this:

`**=SUMIF(A1:A9, "Fuel", B1:B9)**`

But, you could also build in multiple conditions by using the SUMIFS function. SUMIF and SUMIFS are very similar, but SUMIFS can include multiple conditions.

The basic syntax is: 

`=SUMIFS(sum_range, criteria_range1, criterion1, [criteria_range2, criterion2, ...])`

The square brackets let you know that this is optional. The ellipsis at the end of the statement lets you know that you can have as many repetition of these parameters as needed. For example, if you wanted to calculate the sum of the fuel costs for one date in this table, you could create a SUMIFS statement with multiple conditions, like this:

`=SUMIFS(B1:B9, A1:A9, "Fuel", C1:C9, "12/15/2020")`

This formula gives you the total cost of every fuel expense from the date listed in the conditions. In this example, C1:C9 is our second criterion_range and the date 12/15/2020 is the second condition. As long as you follow the basic syntax, you can add up to 127 conditions to a SUMIFS statement!

### COUNTIF to COUNTIFS

Just like the SUMIFS function, COUNTIFS allows you to create a COUNTIF function with multiple conditions.

The basic syntax for COUNTIF is:

`=COUNTIF(range, criterion)`

Just like SUMIF, you set the range and then the condition that needs to be met. For example, if you wanted to count the number of times Food came up in the Expenses column, you could use a COUNTIF function like this:

`=COUNTIF(A1:A9, "Food")`

COUNTIFS have the same basic syntax as SUMIFS:

`**=COUNTIFS(criteria_range1, criterion1, [criteria_range2, criterion2, ...])**`

The criteria_range and criterion are in the same order, and you can add more conditions to the end of the function. So, if you wanted to find the number of times Coffee appeared in the Expenses column on 12/15/2020, you could use COUNTIFS to apply those conditions, like this:

`=COUNTIFS(A1:A9, "Coffee", C1:C9, "12/15/2020")`

This formula follows the basic syntax to create conditions for "Coffee" and the specific date. Now we can find every instance where both of these conditions are true.

For more information
------------------------------------------------------------------------------------------------------------------------------------------------------------------------

SUMIFS and COUNTIFS are just two examples of functions with multiple conditions. They help demonstrate how multiple conditions can be built into the basic syntax of a function. But, there are other functions with multiple conditions that you can use in your data analysis. There are a lot of resources available online to help you get started with these other functions:

-   [How to use the Excel IFS function](https://exceljet.net/excel-functions/excel-ifs-function): This resource includes an explanation and example of the IFS function in Excel. This is a great reference if you are interested in learning more about IFS. The example is a useful way to understand this function and how it can be used.
-   [VLOOKUP in Excel with multiple criteria](https://exceljet.net/formula/vlookup-with-multiple-criteria): Similar to the previous resource, this resource goes into more detail about how to use VLOOKUP with multiple criteria. Being able to apply VLOOKUP with multiple criteria will be a useful skill, so check out this resource for more guidance on how you can start using it on your own spreadsheet data.
-   [INDEX and MATCH in Excel with multiple criteria](https://exceljet.net/formula/index-and-match-with-multiple-criteria): This resource explains how to use the INDEX and MATCH functions with multiple criteria. It also includes an example which helps demonstrate how these functions work with multiple criteria and actual data.
-   [Using IF with AND, OR, and NOT functions in Excel](https://support.microsoft.com/en-us/office/using-if-with-and-or-and-not-functions-d895f58c-b36c-419e-b1f2-5c193a236d97): This resource combines IF with AND, OR, and NOT functions to create more complex functions. By combining these functions, you can perform your tasks more efficiently and cover more criteria at once.