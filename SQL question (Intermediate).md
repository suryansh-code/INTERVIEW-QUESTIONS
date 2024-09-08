# SQL question (Intermediate)

### **32. What are the differences between SQL and PL/SQL?**

Some common differences between SQL and PL/SQL are as shown below:

| **SQL** | **PL/SQL** |
| --- | --- |
| SQL is a query execution or commanding language | PL/SQL is a complete programming language |
| SQL is a data-oriented language. | PL/SQL is a procedural language |
| SQL is very declarative in nature. | PL/SQL has a procedural nature. |
| It is used for manipulating data. | It is used for creating applications. |
| We can execute one statement at a time in SQL | We can execute blocks of statements in PL/SQL |

### **33. What is the difference between BETWEEN and IN operators in SQL?**

**BETWEEN:** The **BETWEEN** operator is used to fetch rows based on a range of values.

For example,

```
SELECT * FROM Students
WHERE ROLL_NO BETWEEN 20 AND 30;
```

This query will select all those rows from the table. Students where the value of the field ROLL_NO lies between 20 and 30.

**IN:** The **IN** operator is used to check for values contained in specific sets.

For example,

```
SELECT * FROM Students
WHERE ROLL_NO IN (20,21,23);
```

This query will select all those rows from the table Students where the value of the field ROLL_NO is either 20 or 21 or 23.

### 34. Write an SQL query to find the names of employees starting with ‘A’.

The LIKE operator of SQL is used for this purpose. It is used to fetch filtered data by searching for a particular pattern in the where clause.

The Syntax for using LIKE is,

> SELECT column1,column2 FROM table_name WHERE column_name LIKE pattern;LIKE: operator namepattern: exact value extracted from the pattern to get related data in result set.
> 

The required query is:

```
SELECT * FROM Employees WHERE EmpName like 'A%' ;
```

You may refer to this article [**WHERE clause**](https://www.geeksforgeeks.org/sql-where-clause) for more details on the LIKE operator.

### 35. What is the difference between primary key and unique constraints?

The primary key cannot have NULL values, the unique constraints can have NULL values. There is only one primary key in a table, but there can be multiple unique constraints. The primary key creates the clustered index automatically but the unique key does not.

### **36. What is a join in SQL? What are the types of joins?**

An SQL Join statement is used to combine data or rows from two or more tables based on a common field between them. Different types of Joins are:

- **INNER JOIN**: The INNER JOIN keyword selects all rows from both tables as long as the condition is satisfied. This keyword will create the result set by combining all rows from both the tables where the condition satisfies i.e. the value of the common field will be the same.
- **LEFT JOIN**: This join returns all the rows of the table on the left side of the join and matching rows for the table on the right side of the join. For the rows for which there is no matching row on the right side, the result set will be null. LEFT JOIN is also known as LEFT OUTER JOIN
- **RIGHT JOIN**: RIGHT JOIN is similar to LEFT JOIN. This join returns all the rows of the table on the right side of the join and matching rows for the table on the left side of the join. For the rows for which there is no matching row on the left side, the result set will contain null. RIGHT JOIN is also known as RIGHT OUTER JOIN.
- **FULL JOIN**: FULL JOIN creates the result set by combining the results of both LEFT JOIN and RIGHT JOIN. The result set will contain all the rows from both tables. For the rows for which there is no matching, the result set will contain NULL values.

### **37. What is an index?**

A database index is a data structure that improves the speed of data retrieval operations on a database table at the cost of additional writes and the use of more storage space to maintain the extra copy of data. Data can be stored only in one order on a disk. To support faster access according to different values, a faster search like a binary search for different values is desired. For this purpose, indexes are created on tables. These indexes need extra space on the disk, but they allow faster search according to different frequently searched values

### 38. What is the On Delete cascade constraint?

An ‘ON DELETE CASCADE’ constraint is used in MySQL to delete the rows from the child table automatically when the rows from the parent table are deleted. For more details, please read [**MySQL – On Delete Cascade constraint**](https://www.geeksforgeeks.org/mysql-on-delete-cascade-constraint) article.

### **39. Explain WITH clause in SQL?**

The `WITH` clause in SQL, also known as **Common Table Expression (CTE)**, allows you to define a temporary result set that can be referenced within a `SELECT`, `INSERT`, `UPDATE`, or `DELETE` statement. It improves readability and can simplify complex queries by breaking them into smaller, more manageable subqueries.

### Syntax:

```sql
sql
Copy code
WITH cte_name AS (
    -- CTE query
    SELECT column1, column2
    FROM table
    WHERE condition
)
SELECT *
FROM cte_name;

```

### Example:

Suppose you have a table `employees` and you want to find the average salary per department and then list only those departments with an average salary greater than 50,000.

```sql
sql
Copy code
WITH department_avg AS (
    SELECT department, AVG(salary) AS avg_salary
    FROM employees
    GROUP BY department
)
SELECT department, avg_salary
FROM department_avg
WHERE avg_salary > 50000;

```

### Benefits of using `WITH` clause:

- **Readability**: Simplifies complex queries.
- **Reusability**: Can be referenced multiple times in the main query.
- **Recursion**: Allows for recursive queries, which is useful for hierarchical data (like organizational structures).

### **0. What are all the different attributes of indexes?**

The indexing has various attributes:

- **Access Types**: This refers to the type of access such as value-based search, range access, etc.
- **Access Time**: It refers to the time needed to find a particular data element or set of elements.
- **Insertion Time**: It refers to the time taken to find the appropriate space and insert new data.
- **Deletion Time**: Time is taken to find an item and delete it as well as update the index structure.
- **Space Overhead**: It refers to the additional space required by the index.

### **41. What is a Cursor?**

The cursor is a Temporary Memory or Temporary Work Station. It is Allocated by Database Server at the Time of Performing DML operations on the Table by the User. Cursors are used to store Database Tables.

### 42. Write down various types of relationships in SQL?

There are various relationships, namely:

- One-to-One Relationship.
- One to Many Relationships.
- Many to One Relationship.
- Self-Referencing Relationship.

### 43. What is a trigger?

**The trigger** is a statement that a system executes automatically when there is any modification to the database. In a trigger, we first specify when the trigger is to be executed and then the action to be performed when the trigger executes. Triggers are used to specify certain integrity constraints and referential constraints that cannot be specified using the constraint mechanism of SQL.

### 44. What is the difference between SQL DELETE and SQL TRUNCATE commands?

| **SQL DELETE** | **SQL TRUNCATE** |
| --- | --- |
| The DELETE statement removes rows one at a time and records an entry in the transaction log for each deleted row. | TRUNCATE TABLE removes the data by deallocating the data pages used to store the table data and records only the page deallocations in the transaction log. |
| DELETE command is slower than the identityTRUNCATE command. | While the TRUNCATE command is faster than the DELETE command. |
| To use Delete you need DELETE permission on the table. | To use Truncate on a table we need at least ALTER permission on the table. |

### 45. What is the difference between Cluster and Non-Cluster Index?

| **CLUSTERED INDEX** | **NON-CLUSTERED INDEX** |
| --- | --- |
| The clustered index is faster. | The non-clustered index is slower. |
| The clustered index requires less memory for operations. | The non-Clustered index requires more memory for operations. |
| In a clustered index, the index is the main data. | In the Non-Clustered index, the index is a copy of data. |
| A table can have only one clustered index. | A table can have multiple non-clustered indexes. |

### 46. What is a Live Lock?

A **livelock** in SQL is a situation where two or more processes continuously change their state in response to each other, but none of them make progress. It’s like a “dancing” scenario where processes keep adjusting, waiting, or retrying but never get to execute successfully.

### Example:

Imagine two people are trying to pass each other in a narrow hallway. Both step left at the same time to avoid collision, then both step right again at the same time. They keep doing this without either of them passing. They aren’t stuck like in a deadlock (where nothing moves), but they keep “moving” without making progress.

In SQL, a livelock can happen when transactions retry too often due to some conflict resolution strategy. For instance:

1. **Transaction A** wants to update Row X.
2. **Transaction B** also wants to update Row X at the same time.
3. Transaction A notices Transaction B and retries.
4. Transaction B also notices Transaction A and retries.
5. Both transactions keep retrying and adjusting without making progress, resulting in a livelock.

Unlike deadlocks, where one process gets stuck until someone breaks the cycle, livelocks involve continuous retries or rollbacks without completing any real work.