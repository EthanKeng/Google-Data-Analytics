Using JOINs effectively
-----------------------

In this reading, you will review how JOINs are used and will be introduced to some resources that you can use to learn more about them. A JOIN combines tables by using a primary or foreign key to align the information coming from both tables in the combination process. JOINs use these keys to identify relationships and corresponding values across tables.

If you need a refresher on primary and foreign keys, refer to the [glossary](https://www.coursera.org/learn/analyze-data/supplement/0p8b6/glossary-terms-and-definitions) for this course, or go back to [Databases in data analytics](https://www.coursera.org/learn/data-preparation/supplement/uXqEX/databases-in-data-analytics).

### [](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.2.Use-JOINS-to-aggregate-data-in-SQL#the-general-join-syntax)The general JOIN syntax

```source-sql
SELECT
	-- table columns from tables are inserted here
	table_name1.column_name
	table_name2.column_name
FROM
	table_name1
JOIN
	table_name2
ON table_name1.column_name = table_name2.column_name
```

As you can see from the syntax, the JOIN statement is part of the FROM clause of the query. JOIN in SQL indicates that you are going to combine data from two tables. ON in SQL identifies how the tables are to be matched for the correct information to be combined from both.

### [](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.2.Use-JOINS-to-aggregate-data-in-SQL#type-of-joins)Type of JOINs

There are four general ways in which to conduct JOINs in SQL queries: INNER, LEFT, RIGHT, and FULL OUTER.

![](https://camo.githubusercontent.com/8bebf254a129030a8c46df144f99fcb23781d10fb984300efef78a894f56c96b/68747470733a2f2f73332e75732d776573742d322e616d617a6f6e6177732e636f6d2f7365637572652e6e6f74696f6e2d7374617469632e636f6d2f37303762333364332d366533332d343266622d626331662d6366643061383235383234362f556e7469746c65642e706e673f582d416d7a2d416c676f726974686d3d415753342d484d41432d53484132353626582d416d7a2d43726564656e7469616c3d414b49415437334c324734354f334b5335325935253246323032313131303725324675732d776573742d322532467333253246617773345f7265717565737426582d416d7a2d446174653d3230323131313037543139323032335a26582d416d7a2d457870697265733d383634303026582d416d7a2d5369676e61747572653d3966306361303238303266316235353835343366313936353135616333646539376436303237316434373237633730623335613865616161366635613835366426582d416d7a2d5369676e6564486561646572733d686f737426726573706f6e73652d636f6e74656e742d646973706f736974696f6e3d66696c656e616d65253230253344253232556e7469746c65642e706e67253232)

The circles represent left and right tables, and where they are joined is highlighted in blue

Here is what these different JOIN queries do.

INNER JOIN

INNER is *optional* in this SQL query because it is the default as well as the most commonly used JOIN operation. You may see this as JOIN only. INNER JOIN returns records if the data lives in both tables. For example, if you use INNER JOIN for the 'customers' and 'orders' tables and match the data using the customer_id key, you would combine the data for each customer_id that exists in both tables. If a customer_id exists in the customers table but not the orders table, data for that customer_id isn't joined or returned by the query.

```source-sql
SELECT
	customers.customer_name,
	orders.product_id,
	orders.ship_date
FROM
	customers
INNER JOIN
	orders
ON customers.customer_id = orders.customer_id
```

The results from the query might look like the following, where customer_name is from the customers table and product_id and ship_date are from the orders table:

| customer_name | product_id | ship_date |
| :-- | :-- | :-- |
| Martin's Ice Cream | 043998 | February 23, 2021 |
| Beachside Treats | 872012 | February 25, 2021 |
| Mona's Natural Flavors | 724956 | February 28, 2021 |
| ... etc. | ... etc. | ... |

The data from both tables was joined together by matching the customer_id common to both tables. Notice that customer_id doesn't show up in the query results. It is simply used to establish the relationship between the data in the two tables so the data can be joined and returned.

LEFT JOIN

You may see this as LEFT OUTER JOIN, but most users prefer LEFT JOIN. Both are correct syntax. LEFT JOIN returns all the records from the left table and only the matching records from the right table. Use LEFT JOIN whenever you need the data from the entire first table and values from the second table, if they exist. For example, in the query below, LEFT JOIN will return customer_name with the corresponding sales_rep, if it is available. If there is a customer who did not interact with a sales representative, that customer would still show up in the query results but with a NULL value for sales_rep.

```source-sql
SELECT
	customers.customer_name,
	sales.sales_rep
FROM
	customers
LEFT JOIN
	sales
ON cutomers.customer_id = sales.customer_id
```

The results from the query might look like the following where customer_name is from the customers table and sales_rep is from the sales table. Again, the data from both tables was joined together by matching the customer_id common to both tables even though customer_id wasn't returned in the query results.

| customer_name | sales_rep |
| :-- | :-- |
| Martin's Ice Cream | Luis Reyes |
| Beachside Treats | NULL |
| Mona's Natural Flavors | Geri Hall |
| ...etc. | ...etc. |

RIGHT JOIN

You may see this as RIGHT OUTER JOIN or RIGHT JOIN. RIGHT JOIN returns all records from the right table and the corresponding records from the left table. Practically speaking, RIGHT JOIN is rarely used. Most people simply switch the tables and stick with LEFT JOIN. But using the previous example for LEFT JOIN, the query using RIGHT JOIN would look like the following:

```source-sql
SELECT	
	sales.sales_rep,
	customers.customer_name
FROM
	sales
RIGHT JOIN
	customers
ON sales.customer_id = customers.customer_id
```

The query results are the same as the previous LEFT JOIN example.

| customer_name | sales_rep |
| :-- | :-- |
| Martin's Ice Cream | Luis Reyes |
| Beachside Treats | NULL |
| Mona's Natural Flavors | Geri Hall |
| ...etc. | ...etc. |

FULL OUTER JOIN

You may sometimes see this as FULL JOIN. FULL OUTER JOIN returns all records from the specified tables. You can combine tables this way, but remember that this can potentially be a large data pull as a result. FULL OUTER JOIN returns all records from *both* tables even if data isn't populated in one of the tables. For example, in the query below, you will get all customers and their products' shipping dates. Because you are using a FULL OUTER JOIN, you may get customers returned without corresponding shipping dates or shipping dates without corresponding customers. A NULL value is returned if corresponding data doesn't exist in either table.

```source-sql
SELECT	
	customers.customer_name,
	orders_ship_date
FROM
	customers
FULL INNER JOIN
	orders
ON customers.customer_id = orders.customer_id
```

The results from the query might look like the following.

| customer_name | ship_date |
| :-- | :-- |
| Martin's Ice Cream | February 23, 2021 |
| Beachside Treats | February 25, 2021 |
| NULL | February 25, 2021 |
| The Daily Scoop | - |
| Mountain Ice Cream | - |
| Mona's Natural Flavors | February 28, 2021 |
| ...etc. | ...etc. |

[](https://github.com/brendensong/Google-Data-Analytics-Professional-Certificate/wiki/5.3.2.Use-JOINS-to-aggregate-data-in-SQL#for-more-information-1)For more information
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------

JOINs are going to be useful for working with relational databases and SQL---and you will have plenty of opportunities to practice them on your own. Here are a few other resources that can give you more information about JOINs and how to use them:

-   [SQL JOINs](https://www.w3schools.com/sql/sql_join.asp): This is a good basic explanation of JOINs with examples. If you need a quick reminder of what the different JOINs do, this is a great resource to bookmark and come back to later.
-   [Database JOINs - Introduction to JOIN Types and Concepts](https://www.essentialsql.com/introduction-database-joins/): This is a really thorough introduction to JOINs. Not only does this article explain what JOINs are and how to use them, but it also explains the various scenarios in more detail of when and why you would use the different JOINs. This is a great resource if you are interested in learning more about the logic behind JOINing.
-   [SQL JOIN Types Explained in Visuals](https://dataschool.com/how-to-teach-people-sql/sql-join-types-explained-visually/): This resource has a visual representation of the different JOINs. This is a really useful way to think about JOINs if you are a visual learner, and it can be a really useful way to remember the different JOINs.
-   [SQL JOINs: Bringing Data Together One Join at a Time](https://towardsdatascience.com/sql-join-8212e3eb9fde): Not only does this resource have a detailed explanation of JOINs with examples, but it also provides example data that you can use to follow along with their step-by-step guide. This is a useful way to practice JOINs with some real data.
-   [SQL JOIN:](https://www.dofactory.com/sql/join) This is another resource that provides a clear explanation of JOINs and uses examples to demonstrate how they work. The examples also combine JOINs with aliasing. This is a great opportunity to see how JOINs can be combined with other SQL concepts that you have been learning about in this course.

