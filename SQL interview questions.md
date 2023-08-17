# [SQL Interview Questions (2023) - GeeksforGeeks](https://www.geeksforgeeks.org/sql-interview-questions/)
# [Advanced SQL Queries, Examples of Queries in SQL List of TOP-70 Items in 2023 - ByteScout](https://bytescout.com/blog/20-important-sql-queries.html)
# What is the difference between BETWEEN and IN operators in [[SQL]]?   
 

**BETWEEN:** The **BETWEEN** operator is used to fetch rows based on a range of values.   
For example, 

```sql
SELECT * FROM Students 
WHERE ROLL_NO BETWEEN 20 AND 30;
```

This query will select all those rows from the table. Students where the value of the field ROLL_NO lies between 20 and 30.   
**IN**   
The **IN** operator is used to check for values contained in specific sets.   
For example, 

```sql
SELECT * FROM Students 
WHERE ROLL_NO IN (20,21,23);
```

This query will select all those rows from the table Students where the value of the field ROLL_NO is either 20 or 21 or 23.
# Write an [[SQL]] query to find the names of employees starting with ‘A’. 

The LIKE operator of SQL is used for this purpose. It is used to fetch filtered data by searching for a particular pattern in the where clause.   
The Syntax for using LIKE is,   
 

```sql
SELECT column1,column2 FROM table_name WHERE column_name LIKE pattern;
```

**LIKE**: operator name
**pattern**: exact value extracted from the pattern to get related data in
result set.

The required query is: 

```sql
SELECT * FROM Employees WHERE EmpName like 'A%' ;
```
# What do you mean by data definition language? 

Data definition language or DDL allows to execution of queries like CREATE, DROP, and ALTER. That is those queries that define the data.

# What do you mean by data manipulation language?

 Data manipulation Language or DML is used to access or manipulate data in the database.   
It allows us to perform the below-listed functions: 

- Insert data or rows in a database
- Delete data from the database
- Retrieve or fetch data
- Update data in a database.
# What is a join in [[SQL]]? What are the types of joins?

An [[SQL]] #Join statement is used to combine data or rows from two or more tables based on a common field between them. Different types of Joins are:
 

- **INNER JOIN**: The INNER JOIN keyword selects all rows from both tables as long as the condition is satisfied. This keyword will create the result set by combining all rows from both the tables where the condition satisfies i.e. the value of the common field will be the same.
- **LEFT JOIN**: This join returns all the rows of the table on the left side of the join and matching rows for the table on the right side of the join. For the rows for which there is no matching row on the right side, the result set will be null. LEFT JOIN is also known as LEFT OUTER JOIN
- **RIGHT JOIN**: RIGHT JOIN is similar to LEFT JOIN. This join returns all the rows of the table on the right side of the join and matching rows for the table on the left side of the join. For the rows for which there is no matching row on the left side, the result set will contain null. RIGHT JOIN is also known as RIGHT OUTER JOIN.
- **FULL JOIN**: FULL JOIN creates the result set by combining the results of both LEFT JOIN and RIGHT JOIN. The result set will contain all the rows from both tables. For the rows for which there is no matching, the result set will contain NULL values.
# Query for Outputting Sorted Data Using ‘Order By’

This query orders the results with respect to the attribute which is referenced using “Order By” – so for example, if that attribute is an integer data type, then the result would either be sorted in ascending or descending order; likewise, if the data type is a String then the result would be ordered in alphabetical order. The order by clause is used to sort the data from the table. The order by clause should always be used in the last of the SQL query.

```sql
SELECT EMP_ID, LAST_NAME FROM EMPLOYEE
WHERE CITY = 'Seattle' ORDER BY EMP_ID;
```

The ordering of the result can also be set manually, using “asc ” for ascending and “desc” for descending.

Ascending (ASC) is the default condition for the ORDER BY clause. In other words, if users don’t specify ASC or DESC after the column name, then the result will be ordered in ascending order only.
```sql
SELECT EMP_ID, LAST_NAME FROM EMPLOYEE_TBL
WHERE CITY = 'INDIANAPOLIS' ORDER BY EMP_ID asc;
```
# SQL Query for Outputting Sorted Data Using 'Group By'
The 'Group By' property groups the resulting data according to the specified attribute.

The [[SQL]] query below will select Name, Age columns from the Patients table, then will filter them by Age value to include records where Age is more than 40 and then will group records with similar Age value and then finally will output them sorted by Name. The basic rule is that the group by clause should always follow a where clause in a Select statement and must precede the Order by clause.

```sql
SELECT Name, Age FROM Patients WHERE Age > 40
GROUP BY Name, Age ORDER BY Name;
```
Another sample of use of Group By: this expression will select records with a price lesser than 70 from the Orders table, will group records with a similar price, will sort the output by price, and will also add the column COUNT(price) that will display how many records with similar price were found:

```sql
SELECT COUNT(price), price FROM orders 
WHERE price < 70 GROUP BY price ORDER BY price
```
Note: you should use the very same set of columns for both SELECT and GROUP BY commands, otherwise you will get an error.