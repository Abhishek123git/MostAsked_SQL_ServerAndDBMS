# SQL, SQL server, DBMS Interview Questions and Answers

_This curated set of 20+ database interview questions reflects the most commonly asked topics across various company interviews I've faced. It includes conceptual questions and practical SQL query challenges designed to test real-world problem-solving skills. Each question is crafted to reinforce core database principles, query optimization techniques, and hands-on SQL proficiency._ 

***These are only technical questions, it is not guaranteed that you will pass the interview if you know all the questions.***

***Note: Those questions are marked ⭐ are most asked.***

1. **Difference between DBMS and RDBMS? ⭐👍**
2. **What is the difference between INNER JOIN, LEFT JOIN, RIGHT JOIN, and FULL JOIN? ⭐**  
3. **What is a primary key and how does it differ from a unique key? ⭐⭐**  
4. **What is a clustered index vs a non-clustered index?**  
5. **What are transactions in SQL and what are ACID properties?**  
6. **What is the difference between DELETE, TRUNCATE, and DROP? ⭐⭐👍**  
7. **What are window functions in SQL and when would you use them?**  
8. **How does a Common Table Expression (CTE) work and how is it different from a subquery? ⭐**  
9. **What are the advantages and disadvantages of using stored procedures? ⭐**
10. **What is the difference between stored procedure and functions? ⭐👍**


## 1. Difference between DBMS and RDBMS

**Answer:** 
- Database Management System is a software that is used to define, create and maintain a database and provide controll to the data.
- RDBMS stands for Relational Database Management System. It is a type of database management system that stores data in a structured format using tables (rows and columns), and enforces relationships between data using keys.

| Feature         | DBMS                          | RDBMS                          |
|----------------|-------------------------------|--------------------------------|
| Data Structure | Hierarchical or navigational  | Tabular (tables with rows/columns) |
| Relationships  | No relationships              | Supports relationships via foreign keys |
| Normalization  | Not enforced                  | Enforced to reduce redundancy |
| Examples       | File System, XML              | SQL Server, MySQL, PostgreSQL |

---

## 2. Difference between INNER JOIN, LEFT JOIN, RIGHT JOIN, and FULL JOIN

| Join Type     | Description |
|---------------|-------------|
| INNER JOIN    | Returns rows with matching values in both tables |
| LEFT JOIN     | Returns all rows from the left table and matched rows from the right |
| RIGHT JOIN    | Returns all rows from the right table and matched rows from the left |
| FULL JOIN     | Returns all rows when there is a match in either table |

---

## 3. Primary Key vs Unique Key

| Feature         | Primary Key                | Unique Key                   |
|----------------|----------------------------|------------------------------|
| Uniqueness     | Ensures unique values      | Ensures unique values        |
| Nulls Allowed  | Not allowed                | Allowed (only one NULL)      |
| Count per Table| Only one                   | Multiple allowed             |
| Purpose        | Entity identification      | Enforce uniqueness           |

---

## 4. Clustered Index vs Non-Clustered Index

| Type              | Clustered Index                         | Non-Clustered Index                     |
|-------------------|------------------------------------------|-----------------------------------------|
| Data Storage      | Sorts and stores data rows physically    | Stores pointers to actual data rows     |
| Count per Table   | Only one                                 | Multiple allowed                        |
| Speed             | Faster for range queries                 | Faster for point queries                |
| Example           | Primary key by default                   | Secondary indexes                       |

---

## 5. Transactions & ACID Properties

- **Transaction**: A unit of work that is performed against a database.
- **ACID**:
  - **Atomicity**: All or nothing
  - **Consistency**: Maintains data integrity
  - **Isolation**: Transactions are independent
  - **Durability**: Changes persist after commit

---

## 6. DELETE vs TRUNCATE vs DROP

| Command   | Deletes Data | Removes Structure | Rollback Possible | Performance |
|-----------|--------------|-------------------|-------------------|-------------|
| DELETE    | ✅            | ❌                 | ✅                 | Slower      |
| TRUNCATE  | ✅ (all rows) | ❌                 | ❌                 | Faster      |
| DROP      | ✅ (all data) | ✅ (table/schema)  | ❌                 | Fastest     |

---

## 7. Window Functions in SQL

- Perform calculations across a set of rows related to the current row.
- Examples: `ROW_NUMBER()`, `RANK()`, `LEAD()`, `LAG()`, `SUM() OVER()`
- Use cases:
  - Ranking
  - Running totals
  - Time-based analysis

---

## 8. Common Table Expression (CTE) vs Subquery

| Feature         | CTE                                | Subquery                          |
|----------------|-------------------------------------|-----------------------------------|
| Readability     | More readable and reusable         | Less readable in complex queries |
| Recursion       | Supports recursion                 | Does not support recursion        |
| Scope           | Temporary result set               | Nested within a query             |

---

## 9. Stored Procedures: Pros & Cons

**Advantages**:
- Reusability
- Improved performance
- Security (parameterized queries)
- Centralized business logic

**Disadvantages**:
- Harder to debug
- Versioning challenges
- Overuse can reduce flexibility

---

## 10. Stored Procedure vs Function

| Feature         | Stored Procedure             | Function                        |
|----------------|------------------------------|----------------------------------|
| Return Type     | Can return zero or more values | Must return a single value       |
| Usage           | Used for performing actions   | Used for computations            |
| Call in SELECT  | ❌                            | ✅                                |
| Transactions    | Can manage transactions       | Cannot manage transactions       |

---
