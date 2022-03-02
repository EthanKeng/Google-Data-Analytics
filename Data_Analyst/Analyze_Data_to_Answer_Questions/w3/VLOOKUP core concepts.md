VLOOKUP core concepts
=====================

Functions can be used to quickly find information and perform calculations using specific values. In this reading, you will learn about the importance of one such function, VLOOKUP, or Vertical Lookup, which searches for a certain value in a spreadsheet column and returns a corresponding piece of information from the row in which the searched value is found.

[](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.1.VLOOKUP-for-data-aggregation#when-do-you-need-to-use-vlookup)When do you need to use VLOOKUP?
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Two common reasons to use VLOOKUP are:

-   Populating data in a spreadsheet
-   Merging data from one spreadsheet with data in another

[](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.1.VLOOKUP-for-data-aggregation#vlookup-syntax)VLOOKUP syntax
------------------------------------------------------------------------------------------------------------------------------------------------------

A VLOOKUP function is available in both Microsoft Excel and Google Sheets. You will be introduced to the general syntax in Google Sheets. (You can refer to the resources at the end of this reading for more information about VLOOKUP in Microsoft Excel.)

`**VLOOKUP(10003, A2:B26, 2, FALSE)**`

Here is the syntax.

`**VLOOKUP(search_key, range, index, [is_sorted])**`

### [](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.1.VLOOKUP-for-data-aggregation#search_key)search_key

-   The value to search for.
-   For example, 42, "Cats", or I24.

### [](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.1.VLOOKUP-for-data-aggregation#range)range

-   The range to consider for the search.
-   The first column in the range is searched to locate data matching the value specified by search_key.

### [](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.1.VLOOKUP-for-data-aggregation#index)index

-   The column index of the value to be returned, where the first column in range is numbered 1.
-   If index is not between 1 and the number of columns in range, #VALUE! is returned.

### [](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.1.VLOOKUP-for-data-aggregation#is_sorted)is_sorted

-   Indicates whether the column to be searched (the first column of the specified range) is sorted. TRUE by default.
-   It's recommended to set is_sorted to FALSE. If set to FALSE, an exact match is returned. If there are multiple matching values, the content of the cell corresponding to the first value found is returned, and #N/A is returned if no such value is found.
-   If is_sorted is TRUE or omitted, the nearest match (less than or equal to the search key) is returned. If all values in the search column are greater than the search key, #N/A is returned.

[](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.1.VLOOKUP-for-data-aggregation#what-if-you-get-na)What if you get #N/A?
-----------------------------------------------------------------------------------------------------------------------------------------------------------------

As you have just read, #N/A indicates that a matching value can't be returned as a result of the VLOOKUP. The error doesn't mean that anything is actually wrong with the data, but people might have questions if they see the error in a report. You can use the IFNA function to replace the #N/A error with something more descriptive, like "Does not exist."

`**IFNA(#N/A, "Does not exist?)**`

Here is the syntax.

`**IFNA(value, value_if_na)**`

### [](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.1.VLOOKUP-for-data-aggregation#value-1)value

-   This is a required value.
-   The function checks if the cell value matches the value; such as #N/A.

### [](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.1.VLOOKUP-for-data-aggregation#value_if_na)value_if_na

-   This is a required value.
-   The function returns this value if the cell value matches the value in the first argument; it returns this value when the cell value is #N/A.

[](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.1.VLOOKUP-for-data-aggregation#helpful-vlookup-reminders)Helpful VLOOKUP reminders
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

-   TRUE means an approximate match, FALSE means an exact match on the search key. If the data used for the search key is sorted, TRUE can be used.
-   You want the column that matches the search key in a VLOOKUP formula to be on the left side of the data. VLOOKUP only looks at data to the right after a match is found. In other words, the index for VLOOKUP indicates columns to the right only. This may require you to move columns around before you use VLOOKUP.
-   After you have populated data with the VLOOKUP formula, you may copy and paste the data as values only to remove the formulas so you can manipulate the data again.

[](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.1.VLOOKUP-for-data-aggregation#vlookup-resources-for-microsoft-excel)VLOOKUP resources for Microsoft Excel
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

VLOOKUP may slightly differ in Microsoft Excel, but the overall concepts can still be generally applied. Refer to the following resources if you are working with Excel.

-   [How to use VLOOKUP in Excel](https://support.microsoft.com/en-us/office/vlookup-function-0bbc8083-26fe-4963-8ab8-93a18ad188a1): This tutorial includes a video to help you get a general understanding of how the VLOOKUP function works in Excel, as well as practical examples to look through.
-   [VLOOKUP in Excel tutorial](https://www.youtube.com/watch?v=d3BYVQ6xIE4): Follow along in this video lesson and learn how to write a VLOOKUP formula in Excel and master time-saving useful tips and tricks.
-   [23 things you should know about VLOOKUP in Excel](https://exceljet.net/things-you-should-know-about-vlookup): Explore this list of 23 VLOOKUP facts as well as challenges you might run into, and start to learn how to master them.
-   [How to use Excel's VLOOKUP function](https://edu.gcfglobal.org/en/excel-tips/how-to-use-excels-vlookup-function/1/): This article shares a specific example around how to apply VLOOKUP in your searches.
-   [VLOOKUP in Excel vs Google Sheets](https://infoinspired.com/sheets-vs-excel-formula/vlookup-formula-in-excel-and-google-sheets/): This guide offers a VLOOKUP comparison of Excel and Google Sheets.

[](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.1.VLOOKUP-for-data-aggregation#test-your-knowledge-on-vlookup)
--------------------------------------------------------------------------------------------------------------------------------------------------------