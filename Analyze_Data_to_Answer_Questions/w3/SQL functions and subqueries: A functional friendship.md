SQL functions and subqueries: A functional friendship
-----------------------------------------------------

### [](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.3.Work-with-subqueries#how-do-sql-functions-function)How do SQL functions, function?

SQL functions are what help make data aggregation possible. (As a reminder, data aggregation is the process of gathering data from multiple sources in order to combine it into a single, summarized collection.) So, how do SQL functions work? Going back to W3Schools, let's review some of these functions to get a better understanding of how to run these queries:

-   [SQL HAVING](http://www-db.deis.unibo.it/courses/TW/DOCS/w3schools/sql/sql_having.asp.html): This is an overview of the HAVING clause, including what it is and a tutorial on how and when it works.
-   [SQL CASE](https://www.w3schools.com/sql/sql_case.asp): Explore the usage of the CASE statement and examples of how it works.
-   [SQL IF](https://www.w3schools.com/sql/func_mysql_if.asp): This is a tutorial of the IF function and offers examples that you can practice with.
-   [SQL COUNT](http://www-db.deis.unibo.it/courses/TW/DOCS/w3schools/sql/sql_func_count.asp.html): The COUNT function is just as important as all the rest, and this tutorial offers multiple examples to review.

### [](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.3.Work-with-subqueries#subqueries---the-cherry-on-top)Subqueries - the cherry on top

Think of a query as a cake. A cake can have multiple layers contained within it and even layers within those layers. Each of these layers are our subqueries, and when you put all of the layers together, you get a cake (query). Usually, you will find subqueries nested in the SELECT, FROM, and/or WHERE clauses. There is no general syntax for subqueries, but the syntax for a basic subquery is as follows:

```source-sql
SELECT account_table.*
FROM (
        SELECT *
        FROM transactino.sf_model_feature_2014_01
        WHERE day_of_week = 'Friday'
    ) account_table
WHERE account_table.availability = 'YES'
```

You will find that, within the first SELECT clause is another SELECT clause. The second SELECT clause marks the start of the subquery in this statement. There are many different ways in which you can make use of subqueries, and resources referenced will provide additional guidance as you learn. But first, let's recap the subquery rules.

There are a few rules that subqueries must follow:

-   Subqueries must be enclosed within parentheses
-   A subquery can have only one column specified in the SELECT clause. But if you want a subquery to compare multiple columns, those columns must be selected in the main query.
-   Subqueries that return more than one row can only be used with multiple value operators, such as the IN operator which allows you to specify multiple values in a WHERE clause.
-   A subquery can't be nested in a SET command. The SET command is used with UPDATE to specify which columns (and values) are to be updated in a table.

### [](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.3.Work-with-subqueries#additional-resources)Additional resources

The following resources offer more guidance into subqueries and their usage:

-   [SQL subqueries:](https://www.w3resource.com/sql/subqueries/understanding-sql-subqueries.php) This detailed introduction includes the definition of a subquery, its purpose in SQL, when and how to use it, and what the results will be
-   [Writing subqueries in SQL](https://mode.com/sql-tutorial/sql-sub-queries/): Explore the basics of subqueries in this interactive tutorial, including examples and practice problems that you can work through

As you continue to learn more about using SQL, functions, and subqueries, you will realize how much time you can truly save when memorizing these tips and tricks.

[](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.3.Work-with-subqueries#test-your-knowledge-on-working-with-subqueries)
----------------------------------------------------------------------------------------------------------------------------------------------------------------