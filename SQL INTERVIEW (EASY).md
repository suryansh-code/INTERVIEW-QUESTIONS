# SQL INTERVIEW (EASY)

### **1.** **What is SQL?**

[**SQL**](https://www.geeksforgeeks.org/sql-tutorial) stands for Structured Query Language. It is a language used to interact with the database, i.e to create a database, to create a table in the database, to retrieve data or update a table in the database, etc.

### **2. What is a database?**

A [**Database**](https://www.geeksforgeeks.org/what-is-database) is defined as a structured form of data storage in a computer or a collection of data in an organized manner and can be accessed in various ways. It is also the collection of schemas, tables, queries, views, etc. Databases help us with easily storing, accessing, and manipulating data held on a computer.

### **3. Does SQL support programming language features?**

It is true that SQL is a language, but it does not support programming as it is not a programming language, it is a command language. We do not have conditional statements in SQL like for loops or if..else, we only have commands which we can use to query, update, delete, etc. data in the database. SQL allows us to manipulate data in a database.

### 4. What is the difference between CHAR and VARCHAR2 datatype in SQL?

Both of these data types are used for characters, but varchar2 is used for character strings of variable length, whereas char is used for character strings of fixed length. **For example**, if we specify the type as char(5) then we will not be allowed to store a string of any other length in this variable, but if we specify the type of this variable as varchar2(5) then we will be allowed to store strings of variable length. We can store a string of length 3 or 4 or 2 in this variable.

### 5. What do you mean by data definition language?

**Data definition language** or DDL allows to execution of queries like CREATE, DROP, and ALTER. That is those queries that define the data.

### 6. What do you mean by data manipulation language?

Data manipulation Language or DML is used to access or manipulate data in the database. It allows us to perform the below-listed functions:

- Insert data or rows in a database
- Delete data from the database
- Retrieve or fetch data
- Update data in a database.

### 7. What is the view in SQL?

[**Views in SQL**](https://www.geeksforgeeks.org/sql-views) are a kind of virtual table. A view also has rows and columns as they are on a real table in the database. We can create a view by selecting fields from one or more tables present in the database. A View can either have all the rows of a table or specific rows based on certain conditions.

### 9. What are table and Field?

**Table:** A table has a combination of rows and columns. Rows are called records and columns are called fields. In MS SQL Server, the tables are being designated within the database and schema names.

**Field:** In DBMS, a database field can be defined as – a single piece of information from a record.

### 10. What is the primary key?

A [**Primary Key](https://www.geeksforgeeks.org/difference-between-primary-and-candidate-key)** is one of the candidate keys. One of the candidate keys is selected as the most important and becomes the primary key. There cannot be more than one primary key in a table.

### **11. What is a Default constraint?**

The [**DEFAULT**](https://www.geeksforgeeks.org/sql-default-constraint) constraint is used to fill a column with default and fixed values. The value will be added to all new records when no other value is provided.

### 12. What is normalization?

It is a process of analyzing the given relation schemas based on their functional dependencies and primary keys to achieve the following desirable properties:

1. Minimizing Redundancy
2. Minimizing the Insertion, Deletion, And Update Anomalies

Relation schemas that do not meet the properties are decomposed into smaller relation schemas that could meet desirable properties.

### **13. What is Denormalization?**

[**Denormalization**](https://www.geeksforgeeks.org/denormalization-in-databases) is a database optimization technique in which we add redundant data to one or more tables. This can help us avoid costly joins in a relational database. Note that denormalization does not mean not doing normalization. It is an optimization technique that is applied after normalization.

### 4. What is a query?

An **SQL** query is used to retrieve the required data from the database. However, there may be multiple SQL queries that yield the same results but with different levels of efficiency. An inefficient query can drain the database resources, reduce the database speed or result in a loss of service for other users. So it is very important to optimize the query to obtain the best database performance.

### **15. What is a subquery?**

In SQL, a [**Subquery**](https://www.geeksforgeeks.org/sql-subquery) can be simply defined as a query within another query. In other words, we can say that a Subquery is a query that is embedded in the WHERE clause of another SQL query.

### 16. What are the different operators available in SQL?

There are three operators available in SQL namely:

1. Arithmetic Operators
2. Logical Operators
3. Comparison Operators

### **17. What is a Constraint?**

Constraints are the rules that we can apply to the type of data in a table. That is, we can specify the limit on the type of data that can be stored in a particular column in a table using constraints. For more details please refer to [**SQL|Constraints**](https://www.geeksforgeeks.org/sql-constraints) article.

### **18. What is Data Integrity?**

Data integrity in DBMS refers to the accuracy, consistency, and reliability of data stored in a database. It ensures that the data remains correct, accurate, and consistent throughout its lifecycle, from initial creation to final deletion. Data integrity is crucial because it prevents data corruption, accidental errors, or malicious tampering, which could compromise the quality and usability of the data.

### 19. What is Auto Increment?

Sometimes, while creating a table, we do not have a unique identifier within the table, hence we face difficulty in choosing Primary Key.

**Auto Increment** in DBMS is a feature used to automatically generate a unique integer value for a column when a new record is inserted into a table. This is typically used for the primary key column to ensure that each record has a unique identifier without requiring manual input.

### 20. What is MySQL collation?

A MySQL collation is a well-defined set of rules which are used to compare characters of a particular character set by using their corresponding encoding

**Collation** in MySQL refers to the set of rules that determine how string comparison and sorting operations are performed. Each character set in MySQL can have one or more collations, which define how characters are compared, sorted, and presented

### 21. What are user-defined functions?

We can use User-defined functions in PL/SQL or Java to provide functionality that is not available in SQL or SQL built-in functions. SQL functions and User-defined functions can appear anywhere, that is, wherever an expression occurs.

For example, it can be used in:

- Select a list of SELECT statements.
- Condition of the WHERE clause.
- CONNECT BY, ORDER BY, START WITH, and GROUP BY
- The VALUES clause of the INSERT statement.
- The SET clause of the UPDATE statement.

### **5. Explain the difference between DELETE and TRUNCATE commands.**

The DELETE command is used by professionals to remove particular rows from a table based on a condition, allowing you to selectively delete records. TRUNCATE, on the other hand, removes all rows from a table without specifying conditions. TRUNCATE is faster and uses fewer system resources than DELETE but does not log individual row deletions.

### **7. What do you mean by a NULL value in SQL?**

A NULL value in SQL represents the absence of data in a column. It is not the same as an empty string or zero; it signifies that the data is missing or unknown. NULL values can be used in columns with optional data or when the actual data is unavailable.

### **10. Explain the differences between SQL and NoSQL databases.**

SQL databases are characterized by their use of structured tables and strict adherence to a predefined schema, making them ideal for managing structured data with a strong focus on data consistency and transaction support. In contrast, [NoSQL](https://www.simplilearn.com/rise-of-nosql-and-why-it-should-matter-to-you-article) databases are non-relational and excel in handling unstructured or semi-structured data, frequently employed for scalable, distributed, and adaptable data storage solutions.

### **0. Explain the differences between SQL and NoSQL databases.**

The difference between SQL and NoSQL databases primarily revolves around their data models, scalability, schema flexibility, and use cases. Here's a comparison:

### 1. **Data Model**:

- **SQL Databases**:
    - **Relational**: Data is stored in structured tables with predefined schemas, where rows represent records and columns represent attributes.
    - **Schema**: Strongly enforced, meaning every record must adhere to the table structure.
    - **Examples**: MySQL, PostgreSQL, Oracle, SQL Server.
- **NoSQL Databases**:
    - **Non-relational**: Data can be stored in various formats such as documents (JSON), key-value pairs, wide-column stores, or graphs.
    - **Schema**: Schema-less or flexible schema, allowing for unstructured or semi-structured data.
    - **Examples**: MongoDB (document-based), Cassandra (wide-column store), Redis (key-value store), Neo4j (graph database).

### **16. What are indexes in SQL?**

Indexes improve the data retrieval operations speed. They provide a quick way to locate specific rows in a table by creating a sorted data structure based on one or more columns. Indexes are essential for optimizing query performance.

### **17. Explain GROUP BY in SQL.**

The GROUP BY clause organizes rows from a table into groups based on the values in one or more columns. It is commonly employed alongside aggregate functions like SUM, COUNT, AVG, MIN, and MAX to perform computations on data that has been grouped together.

### **18. What is an SQL alias?**

An SQL alias is a temporary name you give to a table or column in a query to make it easier to reference or to make your query more readable.

For example:

- If you have a column named `first_name`, you can give it an alias like `fn` for simplicity.
- If you have a table called `employees`, you can give it an alias like `e`.

Here’s how you do it:

```sql
sqlCopy code
SELECT first_name AS fn FROM employees AS e;

```

In this query:

- `fn` is the alias for `first_name`.
- `e` is the alias for `employees`.

Aliases don't change the actual name of the column or table; they just make your query easier to read and write.

### **19. Explain ORDER BY in SQL.**

The ORDER BY clause is used to sort the result set of a query based on one or more columns. You can specify each column's sorting order (ascending or descending). For example:

SELECT * FROM products ORDER BY price DESC;

### 20.What is the difference between where and Having clause

he `WHERE` and `HAVING` clauses in SQL are both used to filter records, but they are applied at different stages of query processing and serve different purposes:

### 1. **WHERE Clause**:

- **Purpose**: Filters rows before any grouping or aggregation takes place.
- **Use**: Typically used to filter individual rows based on a condition.
- **Applies To**: Raw data before aggregation.
- **Example**:This query retrieves all employees with a salary greater than 50,000.
    
    ```sql
    sqlCopy code
    SELECT * FROM employees
    WHERE salary > 50000;
    
    ```
    

### 2. **HAVING Clause**:

- **Purpose**: Filters groups after aggregation has taken place.
- **Use**: Used to filter the results of an aggregate function like `SUM`, `COUNT`, `AVG`, etc.
- **Applies To**: Aggregated data after the `GROUP BY` clause.
- **Example**:This query counts the number of employees in each department and then filters to only show departments with more than 5 employees.
    
    ```sql
    sqlCopy code
    SELECT department, COUNT(*) as num_employees
    FROM employees
    GROUP BY department
    HAVING COUNT(*) > 5;
    
    ```
    

### Summary:

- Use `WHERE` to filter records **before** aggregation.
- Use `HAVING` to filter groups **after** aggregation.

### 24. What are aggregate and scalar functions?

For doing operations on data SQL has many built-in functions, they are categorized into two categories and further sub-categorized into seven different functions under each category. The categories are:

- **Aggregate functions:** These functions are used to do operations from the values of the column and a single value is returned.
- **Scalar functions:** These functions are based on user input, these too return a single value.

### 25. What is an ALIAS command?

Aliases are the temporary names given to a table or column for the purpose of a particular SQL query. It is used when the name of a column or table is used other than its original name, but the modified name is only temporary.

- Aliases are created to make table or column names more readable.
- The renaming is just a temporary change and the table name does not change in the original database.
- Aliases are useful when table or column names are big or not very readable.
- These are preferred when there is more than one table involved in a query.

### 26. What are Union, minus, and Interact commands?

Set Operations in SQL eliminate duplicate tuples and can be applied only to the relations which are union compatible. Set Operations available in SQL are :

- Set Union
- Set Intersection
- Set Difference

**UNION Operation:** This operation includes all the tuples which are present in either of the relations. For example: To find all the customers who have a loan or an account or both in a bank.

```
 SELECT CustomerName FROM Depositor
 UNION
 SELECT CustomerName FROM Borrower ;
```

The union operation automatically eliminates duplicates. If all the duplicates are supposed to be retained, UNION ALL is used in place of UNION.

**INTERSECT Operation:** This operation includes the tuples which are present in both of the relations. For example: To find the customers who have a loan as well as an account in the bank:

```
 SELECT CustomerName FROM Depositor
 INTERSECT
 SELECT CustomerName FROM Borrower ;
```

The Intersect operation automatically eliminates duplicates. If all the duplicates are supposed to be retained, INTERSECT ALL is used in place of INTERSECT.

**EXCEPT for Operation:** This operation includes tuples that are present in one relationship but should not be present in another relationship. For example: To find customers who have an account but no loan at the bank:

```
 SELECT CustomerName FROM Depositor
 EXCEPT
 SELECT CustomerName FROM Borrower ;
```

The Except operation automatically eliminates the duplicates. If all the duplicates are supposed to be retained, EXCEPT ALL is used in place of EXCEPT.

### 27. What is a T-SQL?

T-SQL is an abbreviation for Transact Structure Query Language. It is a product by Microsoft and is an extension of SQL Language which is used to interact with relational databases. It is considered to perform best with Microsoft SQL servers. T-SQL statements are used to perform the transactions to the databases. T-SQL has huge importance since all the communications with an instance of an SQL server are done by sending Transact-SQL statements to the server. Users can also define functions using T-SQL.

Types of T-SQL functions are :

- **Aggregate** functions.
- **Ranking** functions. There are different types of ranking functions.
- **Rowset** function.
- **Scalar** functions.

### 28. What is ETL in SQL?

ETL is a process in Data Warehousing and it stands for **Extract**, **Transform,** and **Load**. It is a process in which an ETL tool extracts the data from various data source systems, transforms it in the staging area, and then finally, loads it into the Data Warehouse system. These are three database functions that are incorporated into one tool to pull data out from one database and put data into another database.

### 28. What is ETL in SQL?

ETL is a process in Data Warehousing and it stands for **Extract**, **Transform,** and **Load**. It is a process in which an ETL tool extracts the data from various data source systems, transforms it in the staging area, and then finally, loads it into the Data Warehouse system. These are three database functions that are incorporated into one tool to pull data out from one database and put data into another database.

### 29. How to copy tables in SQL?

Sometimes, in SQL, we need to create an exact copy of an already defined (or created) table. [**MySQL**](https://www.geeksforgeeks.org/sql-tutorial/#mysql) enables you to perform this operation. Because we may need such duplicate tables for testing the data without having any impact on the original table and the data stored in it.

```
CREATE TABLE Contact List(Clone_1) LIKE Original_table;
```

For more details, Please read [**Cloning Table in**](https://www.geeksforgeeks.org/cloning-table-in-mysql) the [**MySQL**](https://www.geeksforgeeks.org/cloning-table-in-mysql) article.

### 30. What is SQL injection?

SQL injection is a technique used to exploit user data through web page inputs by injecting SQL commands as statements. Basically, these statements can be used to manipulate the application’s web server by malicious users.

- SQL injection is a code injection technique that might destroy your database.
- SQL injection is one of the most common web hacking techniques.
- SQL injection is the placement of malicious code in SQL statements, via web page input.

### 31. Can we disable a trigger? If yes, how?

Yes, we can disable a trigger in PL/SQL. If consider temporarily disabling a trigger and one of the following conditions is true:

- An object that the trigger references is not available.
- We must perform a large data load and want it to proceed quickly without firing triggers.
- We are loading data into the table to which the trigger applies.
- We disable a trigger using the ALTER TRIGGER statement with the DISABLE option.
- We can disable all triggers associated with a table at the same time using the ALTER TABLE statement with the DISABLE ALL TRIGGERS option.