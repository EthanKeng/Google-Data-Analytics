Manipulating strings in SQL
===========================

Knowing how to convert and manipulate your data for an accurate analysis is an important part of a data analyst's job. In this reading, you will learn about different SQL functions and their usage, especially regarding string combinations.

A string is a set of characters that helps to declare the texts in programming languages such as SQL. SQL string functions are used to obtain various information about the characters, or in this case, manipulate them. One such function, CONCAT, is commonly used. Review the table below to learn more about the CONCAT function and its variations.

| Function | Usage | Example |
| :-- | :-- | :-- |
| CONCAT | A function that adds strings together to create new text strings that can be used as unique keys | CONCAT ('Google', '.com'); |
| CONCAT_WS | A function that adds two or more strings together with a separator | CONCAT_WS (' . ', 'www', 'google', 'com')

*The separator (being the period) gets input before and after Google when you run the SQL function |
| CONCAT with + | Adds two or more strings together using the + operator | 'Google' + '.com' |

[](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.2.2.Combine-multiple-datasets#concat-at-work)CONCAT at work
---------------------------------------------------------------------------------------------------------------------------------------------------

When adding two strings together such as 'Data' and 'analysis', it will be input like this:

-   SELECT CONCAT ('Data', 'analysis');

The result will be:

-   Dataanalysis

Sometimes, depending on the strings, you will need to add a space character, so your function should actually be:

-   SELECT CONCAT ('Data', ' ', 'analysis');

And the result will be:

-   Data analysis

The same rule applies when combining three strings together. For example,

-   SELECT CONCAT ('Data',' ', 'analysis', ' ', 'is', ' ', 'awesome!');

And the result will be

-   Data analysis is awesome!

[](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.2.2.Combine-multiple-datasets#practice-makes-perfect)Practice makes perfect
-------------------------------------------------------------------------------------------------------------------------------------------------------------------

W3 Schools is an excellent resource for interactive SQL learning, and the following links will guide you through transforming your data using SQL:

-   [SQL functions](https://www.w3schools.com/sql/sql_ref_sqlserver.asp): This is a comprehensive list of functions to get you started. Click on each function, where you will learn about the definition, usage, examples, and even be able to create and run your own query for practice. Try it out for yourself!
-   [SQL Keywords](https://www.w3schools.com/sql/sql_ref_keywords.asp): This is a helpful SQL keywords reference to bookmark as you increase your knowledge of SQL. This list of keywords are reserved words that you will use as your need to perform different operations in the database grows.
-   While this reading went through the basics of each of these functions, there is still more to learn, and you can even combine your own strings.

1.  Practice using [CONCAT](https://www.w3schools.com/sql/func_sqlserver_concat.asp)
2.  Practice using [CONCAT WS](https://www.w3schools.com/sql/func_sqlserver_concat_ws.asp)
3.  Practice using [CONCAT with +](https://www.w3schools.com/sql/func_sqlserver_concat_with_plus.asp)

Pro tip: The functions presented in the resources above may be applied in slightly different ways depending on the database that you are using (e.g. mySQL versus SQL Server). But, the general description provided for each function will prepare you to customize how you use these functions as needed.

