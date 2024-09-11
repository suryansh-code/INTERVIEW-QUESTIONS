# SQL question (Advance)

## 48. Name different types of case manipulation functions available in SQL.

There are three types of case manipulation functions available in SQL. They are,

- **LOWER**: The purpose of this function is to return the string in lowercase. It takes a string as an argument and returns the string by converting it into lower case. **Syntax:**

> LOWER(‘string’)
> 
- **UPPER**: The purpose of this function is to return the string in uppercase. It takes a string as an argument and returns the string by converting it into uppercase. **Syntax:**

> UPPER(‘string’)
> 
- **INITCAP**: The purpose of this function is to return the string with the first letter in uppercase and the rest of the letters in lowercase. **Syntax:**

> INITCAP(‘string’)
> 

### 49. What are local and global variables and their differences?

**Global Variable:** In contrast, global variables are variables that are defined outside of functions. These variables have global scope, so they can be used by any function without passing them to the function as parameters.

**Local Variable:** Local variables are variables that are defined within functions. They have local scope, which means that they can only be used within the functions that define them.

### 50. Name the function which is used to remove spaces at the end of a string?

In SQL, the spaces at the end of the string are removed by a trim function.

**Syntax:**

> Trim(s) , Where s is a any string.
> 

### 51. What is the difference between TRUNCATE and DROP statements?

| **SQL DROP** | **TRUNCATE** |
| --- | --- |
| The DROP command is used to remove the table definition and its contents. | Whereas the TRUNCATE command is used to delete all the rows from the table. |
| In the DROP command, table space is freed from memory. | While the TRUNCATE command does not free the table space from memory. |
| DROP is a DDL(Data Definition Language) command. | Whereas the TRUNCATE is also a DDL(Data Definition Language) command. |
| In the DROP command, a view of the table does not exist. | While in this command, a view of the table exists. |
| In the DROP command, integrity constraints will be removed. | While in this command, integrity constraints will not be removed. |

### **52. Which operator is used in queries for pattern matching?**

LIKE operator: It is used to fetch filtered data by searching for a particular pattern in the where clause.

**Syntax:**

> SELECT column1,column2 FROM table_name WHERE column_name LIKE pattern;LIKE: operator name
> 

### **53. Define SQL Order by the statement?**

The ORDER BY statement in SQL is used to sort the fetched data in either ascending or descending according to one or more columns.

- By default ORDER BY sorts the data in **ascending order.**
- We can use the keyword DESC to sort the data in descending order and the keyword ASC to sort in ascending order.

### **54. Explain SQL Having statement?**

HAVING is used to specify a condition for a group or an aggregate function used in the select statement. The WHERE clause selects before grouping. The HAVING clause selects rows after grouping. Unlike the HAVING clause, the WHERE clause cannot contain aggregate functions. See [**Having vs Where Clause?**](https://www.geeksforgeeks.org/having-vs-where-clause-in-sql)

### 55. Explain SQL AND OR statement with an example?

In SQL, the AND & OR operators are used for filtering the data and getting precise results based on conditions. The AND and OR operators are used with the WHERE clause.

These **two operators** are called **conjunctive operators**.

1. **AND Operator:** This operator displays only those records where both conditions **condition 1 and condition 2 evaluate to True.**
2. **OR Operator:** This operator displays the records where either one of the conditions condition 1 and condition 2 evaluates to True. That is, **either condition1 is True or condition2 is True.**

### 56. Define BETWEEN statements in SQL?

The SQL BETWEEN condition allows you to easily test if an expression is within a range of values (inclusive). The values can be text, date, or numbers. It can be used in a SELECT, INSERT, UPDATE, or DELETE statement. The SQL BETWEEN Condition will return the records where the expression is within the range of value1 and value2.

### **57. Why do we use Commit and Rollback commands?**

| **COMMIT** | **ROLLBACK** |
| --- | --- |
| COMMIT permanently saves the changes made by the current transaction. | ROLLBACK undo the changes made by the current transaction. |
| The transaction can not undo changes after COMMIT execution. | Transaction reaches its previous state after ROLLBACK. |
| When the transaction is successful, COMMIT is applied. | When the transaction is aborted, ROLLBACK occurs. |

### 58. What are ACID properties?

A [**transaction**](https://www.geeksforgeeks.org/sql-transactions) is a single logical unit of work that accesses and possibly modifies the contents of a database. Transactions access data using read-and-write operations. In order to maintain consistency in a database, before and after the transaction, certain properties are followed. These are called **ACID** properties. **ACID** (Atomicity, Consistency, Isolation, Durability) is a set of properties that guarantee that database transactions are processed reliably. For more details please read [**ACID properties in**](https://www.geeksforgeeks.org/acid-properties-in-dbms) the [**DBMS**](https://www.geeksforgeeks.org/acid-properties-in-dbms) article.

### 59. Are NULL values the same as zero or a blank space?

In SQL, zero or blank space can be compared with another zero or blank space. whereas one null may not be equal to another null. null means data might not be provided or there is no data.

### 60. What is the need for group functions in SQL?

In database management, group functions, also known as aggregate functions,  is a function where the values of multiple rows are grouped together as input on certain criteria to form a single value of more significant meaning.

**Various Group Functions**

```
1) Count()
2) Sum()
3) Avg()
4) Min()
```

### 61. What is the need for a MERGE statement?

The **MERGE** command in SQL is actually a combination of three SQL statements: **INSERT, UPDATE, and DELETE**. In simple words, the MERGE statement in SQL provides a convenient way to perform all these three operations together which can be very helpful when it comes to handling large running databases. But unlike INSERT, UPDATE, and DELETE statements MERGE statement requires a source table to perform these operations on the required table which is called a target table.

### 62. How can you fetch common records from two tables?

The below statement could be used to get data from multiple tables, so, we need to use join to get data from multiple tables.

**Syntax :**

> SELECT tablenmae1.colunmname, tablename2.columnnmaeFROM tablenmae1JOIN tablename2ON tablenmae1.colunmnam = tablename2.columnnmaeORDER BY columnname;
> 

### 63. What are the advantages of PL/SQL functions?

The advantages of PL / SQL functions are as follows:

- We can make a single call to the database to run a block of statements. Thus, it improves the performance against running SQL multiple times. This will reduce the number of calls between the database and the application.
- We can divide the overall work into small modules which becomes quite manageable, also enhancing the readability of the code.
- It promotes reusability.
- It is secure since the code stays inside the database, thus hiding internal database details from the application(user). The user only makes a call to the PL/SQL functions. Hence, security and data hiding is ensured.

### 64. What is the SQL query to display the current date?

CURRENT_DATE returns to the current date. This function returns the same value if it is executed more than once in a single statement, which means that the value is fixed, even if there is a long delay between fetching rows in a cursor.

Syntax:

> CURRENT_DATEorCURRENT DATE
> 

### 65. What are Nested Triggers?

In SQL, a "nested trigger" refers to the situation where one trigger's actions cause another trigger to fire, which in turn might lead to yet another trigger firing, and so on. This nesting can occur in various scenarios where triggers are involved.

Here’s a breakdown of nested triggers:

### **What Triggers Are:**

- **Triggers** are special types of stored procedures that are automatically executed or fired when certain events occur on a table or view (such as INSERT, UPDATE, or DELETE operations).

### **How Nesting Occurs:**

- A **nested trigger** happens when an action performed by one trigger causes another trigger to fire. For example, an UPDATE trigger on Table A might perform an action that results in an UPDATE on Table B, which has its own trigger. This can lead to a chain reaction of triggers.

### 66. How to find the available constraint information in the table?

In SQL Server the **data dictionary** is a set of database tables used to store information about a database’s definition. One can use these data dictionaries to check the constraints on an already existing table and to change them(if possible). For more details please read [**SQL | Checking Existing Constraint on a table**](https://www.geeksforgeeks.org/sql-checking-existing-constraints-on-a-table-using-data-dictionaries) article.

### 67. How do we avoid getting duplicate entries in a query without using the distinct keyword?

DISTINCT is useful in certain circumstances, but it has drawbacks that it can increase the load on the query engine to perform the sort (since it needs to compare the result set to itself to remove duplicates). We can remove duplicate entries using the following options:

- Remove duplicates using row numbers.
- Remove duplicates using self-Join.
- Remove duplicates using group by.

### 68. The difference between NVL and NVL2 functions?

In SQL, `NVL` and `NVL2` are functions used to handle NULL values, but they have different use cases and functionalities. Here’s a detailed comparison:

### **1. NVL Function:**

- **Purpose:** The `NVL` function is used to replace NULL values with a specified value.
- **Syntax:**
    
    ```sql
    sql
    Copy code
    NVL(expression, replacement)
    
    ```
    
- **Parameters:**
    - `expression`: The value to be checked for NULL.
    - `replacement`: The value to return if `expression` is NULL.
- **Example:**
    
    ```sql
    sql
    Copy code
    SELECT NVL(salary, 0) AS adjusted_salary
    FROM employees;
    
    ```
    
    This query will return the `salary` if it's not NULL; otherwise, it will return 0.
    

### **2. NVL2 Function:**

- **Purpose:** The `NVL2` function provides more flexibility compared to `NVL`. It allows you to specify different values for when the expression is NULL and when it is not NULL.
- **Syntax:**
    
    ```sql
    sql
    Copy code
    NVL2(expression, value_if_not_null, value_if_null)
    
    ```
    
- **Parameters:**
    - `expression`: The value to be checked for NULL.
    - `value_if_not_null`: The value to return if `expression` is not NULL.
    - `value_if_null`: The value to return if `expression` is NULL.
- **Example:**
    
    ```sql
    sql
    Copy code
    SELECT NVL2(salary, salary * 1.1, 0) AS adjusted_salary
    FROM employees;
    
    ```
    
    This query will return `salary * 1.1` if `salary` is not NULL; otherwise, it will return 0.
    

### **Key Differences:**

1. **Number of Return Values:**
    - **NVL:** Only allows you to specify what value to return when the expression is NULL. There is no option to specify a return value if the expression is not NULL.
    - **NVL2:** Allows you to specify different return values for both NULL and non-NULL cases.
2. **Flexibility:**
    - **NVL:** Limited to replacing NULL with a single specified value.
    - **NVL2:** Provides greater flexibility by allowing you to define different outcomes based on whether the expression is NULL or not.

### **Usage Examples:**

- **NVL Example:**
If you have a column `commission` that may contain NULL values and you want to treat those NULLs as 0, use:
    
    ```sql
    sql
    Copy code
    SELECT NVL(commission, 0) AS commission_amount
    FROM sales;
    
    ```
    
- **NVL2 Example:**
If you want to apply a different logic when the `commission` is NULL versus when it's not NULL, such as applying a 10% bonus to non-NULL values and using 0 for NULLs:
    
    ```sql
    sql
    Copy code
    SELECT NVL2(commission, commission * 1.1, 0) AS adjusted_commission
    FROM sales;
    
    ```
    

Understanding the difference between `NVL` and `NVL2` allows you to handle NULL values more effectively based on your specific needs.

### 69.  What is the difference between COALESCE() & ISNULL()? 
explain in short and in easy language please

Certainly! Both `COALESCE()` and `ISNULL()` are used to handle NULL values in SQL, but they have some differences. Here’s a simplified comparison:

### **1. COALESCE() Function:**

- **Purpose:** Returns the first non-NULL value from a list of arguments.
- **Syntax:**
    
    ```sql
    sql
    Copy code
    COALESCE(value1, value2, value3, ...)
    
    ```
    
- **How It Works:** Checks each value in the list from left to right. Returns the first value that is not NULL. If all values are NULL, it returns NULL.
- **Example:**
    
    ```sql
    sql
    Copy code
    SELECT COALESCE(commission, bonus, 0) AS final_value
    FROM employees;
    
    ```
    
    This returns the value of `commission` if it's not NULL; if `commission` is NULL, it checks `bonus`; if `bonus` is also NULL, it returns 0.
    
- **Key Point:** You can use multiple values in `COALESCE()`, and it’s part of the SQL standard, so it works across different SQL databases.

### **2. ISNULL() Function:**

- **Purpose:** Replaces NULL with a specified value.
- **Syntax:**
    
    ```sql
    sql
    Copy code
    ISNULL(expression, replacement)
    
    ```
    
- **How It Works:** Checks if `expression` is NULL. If it is, it returns `replacement`; otherwise, it returns `expression`.
- **Example:**
    
    ```sql
    sql
    Copy code
    SELECT ISNULL(commission, 0) AS final_value
    FROM employees;
    
    ```
    
    This returns the value of `commission` if it's not NULL; otherwise, it returns 0.
    
- **Key Point:** `ISNULL()` typically supports only two arguments and is specific to SQL Server. Other databases might have similar functions with different names, like `NVL()` in Oracle.

###