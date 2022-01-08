More about spreadsheet errors and fixes
=======================================


When you are new to data analytics---and sometimes even when you aren't---spreadsheet struggles are real. It never feels good when you type in what you are sure is a perfect formula or function, only to get an error message. Understanding errors and how to fix them is a big part of keeping your data clean, so it's important to know how to deal with issues as they come up, and more importantly, not to get discouraged.

Remember, even the most advanced spreadsheet users come across problems from time to time.  

![This illustration shows one nervous woman handing another woman a stack of papers with a question mark on them. ](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/15aGB_eRSfWWhgf3kWn1rg_b360212c1d574fb7990ff1eebb375605_Screen-Shot-2020-12-11-at-8.04.43-AM.png?expiry=1641772800000&hmac=ablGnb3h11c-oocgoxNyfF2Kvv58EJvYwye4cD0y02U)

As a follow-up to what you learned in the previous video, here are a few best practices and helpful tips. These strategies will help you avoid spreadsheet errors to begin with, making your life in analytics a whole lot less stressful:

1.  Filter data to make your spreadsheet less complex and busy.

2.  Use and freeze headers so you know what is in each column, even when scrolling.

3.  When multiplying numbers, use an asterisk (*) not an X.

4.  Start every formula and function with an equal sign (=).

5.  Whenever you use an open parenthesis, make sure there is a closed parenthesis on the other end to match.

6.  Change the font to something easy to read.

7.  Set the border colors to white so that you are working in a blank sheet. 

8.  Create a tab with just the raw data, and a separate tab with just the data you need.

Now that you have learned some basic ways to avoid errors, you can focus on what to do when that dreaded pop-up does appear. The following table is a reference you can use to look up common spreadsheet errors and examples of each. Knowing what the errors mean takes some of the fear out of getting them.

| Error | Description | Example |
| --- | --- | --- |
| #DIV/0! | A formula is trying to divide a value in a cell by 0 (or an empty cell with no value) | =B2/B3, when the cell B3 contains the value 0 |
| #ERROR! | (Google Sheets only) Something can't be interpreted as it has been input. This is also known as a parsing error. | =COUNT(B1:D1 C1:C10) is invalid because the cell ranges aren't separated by a comma |
| #N/A | A formula can't find the data | The cell being referenced can't be found |
| #NAME? | The name of a formula or function used isn't recognized | The name of a function is misspelled |
| #NUM! | The spreadsheet can't perform a formula calculation because a cell has an invalid numeric value | =DATEDIF(A4, B4, "M") is unable to calculate the number of months between two dates because the date in cell A4 falls after the date in cell B4 |
| #REF! | A formula is referencing a cell that isn't valid | A cell used in a formula was in a column that was deleted |
| #VALUE! | A general error indicating a problem with a formula or with referenced cells | There could be problems with spaces or text, or with referenced cells in a formula; you may have additional work to find the source of the problem. |

If you are working with Microsoft Excel, an interactive page, [How to correct a #VALUE! error](https://support.microsoft.com/en-us/office/how-to-correct-a-value-error-15e1b616-fbf2-4147-9c0b-0a11a20e409e "How to correct a #VALUE! error"), can help you narrow down the cause of this error. You can select a specific function from a drop-down list to display a link to tips to fix the error when using that function.

Pro tip: Spotting errors in spreadsheets with conditional formatting
--------------------------------------------------------------------

Conditional formatting can be used to highlight cells a different color based on their contents. This feature can be extremely helpful when you want to locate all errors in a large spreadsheet. For example, using conditional formatting, you can highlight in yellow all cells that contain an error, and then work to fix them.

### Conditional formatting in Microsoft Excel

To set up conditional formatting in Microsoft Excel to highlight all cells in a spreadsheet that contain errors, do the following:

1.  Click the gray triangle above row number 1 and to the left of Column A to select all cells in the spreadsheet.

2.  From the main menu, click Home, and then click Conditional Formatting to select Highlight Cell Rules > More Rules.

3.  For Select a Rule Type, choose Use a formula to determine which cells to format.

4.  For Format values where this formula is true, enter =ISERROR(A1).

5.  Click the Format button, select the Fill tab, select yellow (or any other color), and then click OK.

6.  Click OK to close the format rule window.

To remove conditional formatting, click Home and select Conditional Formatting, and then click Manage Rules. Locate the format rule in the list, click Delete Rule, and then click OK.

### Conditional formatting in Google Sheets

To set up conditional formatting in Google Sheets to highlight all cells in a spreadsheet that contain errors, do the following:

1.  Click the empty rectangle above row number 1 and to the left of Column A to select all cells in the spreadsheet. In the [Step-by-step in spreadsheets](https://www.coursera.org/learn/ask-questions-make-decisions/lecture/lpuHf/step-by-step-in-spreadsheets "Step-by-step in spreadsheets") video, this was called the Select All button.

2.  From the main menu, click Format and select Conditional Formatting to open the Conditional format rules pane on the right.

3.  While in the Single Color tab, under Format rules, use the drop-down to select Custom formula is, enter =ISERROR(A1), select yellow (or any other color) for the formatting style, and then click Done.

To remove conditional formatting, click Format and select Conditional Formatting, and then click the Trash icon for the format rule.

Spreadsheet error resources
---------------------------

To learn more and read about additional examples of errors and solutions, explore these resources:

-   [Microsoft Formulas and Functions](https://support.microsoft.com/en-us/office/formulas-and-functions-294d9486-b332-48ed-b489-abe7d0f9eda9?ui=en-US&rs=en-US&ad=US#id0eaabaaa=errors "Microsoft Forumulas and Functions"): This resource describes how to avoid broken formulas and how to correct errors in Microsoft Excel. This is a useful reference to have saved in case you run into a specific error and need to find solutions quickly while working in Excel. 

-   [When Your Formula Doesn't Work: Formula Parse Errors in Google Sheets](https://www.benlcollins.com/spreadsheets/formula-parse-error/ "When Your Formula Doesn't Work: Formula Parse Errors in Google Sheets"): This resource is a guide to finding and fixing some common errors in Google Sheets. If you are working with Google Sheets, you can use this as a quick reference for solving problems you might encounter working on your own.

With some practice and investigative determination, you will become much more comfortable handling errors in spreadsheets. Each error you catch and fix will make your data clearer, cleaner, and more useful.