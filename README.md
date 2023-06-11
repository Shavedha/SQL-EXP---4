# SQL - EXPERIMENT 4 - To create an SQL query to show record from one table that another table does not have.
## AIM
To create an SQL query to show record from one table that another table does not have.
## ALGORITHM
1. Create two tables named "table1" and "table2". Both tables have the same columns: id, name, department, and salary.
2. Insert sample data into both tables.
3. Use the SELECT statement with a NOT IN subquery to retrieve records from table1 that do not exist in table2 based on the id column comparison.
4. Retrieve the records from table1 that are not present in table2 based on the id column comparison.
5. End the program
## PROGRAM
```
-- Connect to your database
-- Example: For MySQL, use the following command:
-- mysql -u your_username -p your_database_name

-- Create the first table
CREATE TABLE table1 (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    department VARCHAR(50),
    salary DECIMAL(10, 2)
);

-- Create the second table
CREATE TABLE table2 (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    department VARCHAR(50),
    salary DECIMAL(10, 2)
);

-- Insert sample data into the first table
INSERT INTO table1 (id, name, department, salary)
VALUES (1, 'John Doe', 'Sales', 5000),
       (2, 'Jane Smith', 'Marketing', 6000),
       (3, 'David Johnson', 'IT', 7000),
       (4, 'Emily Brown', 'Finance', 5500),
       (5, 'Michael Davis', 'HR', 4500);

-- Insert sample data into the second table
INSERT INTO table2 (id, name, department, salary)
VALUES (1, 'John Doe', 'Sales', 5000),
       (3, 'David Johnson', 'IT', 7000),
       (5, 'Michael Davis', 'HR', 4500);

-- Retrieve records from table1 that do not exist in table2
SELECT *
FROM table1
WHERE id NOT IN (
    SELECT id
    FROM table2
);

```
## OUTPUT
<img width="458" alt="image" src="https://github.com/Shavedha/SQL-EXP---4/assets/93427376/b9fbaa4d-7d3b-4054-a1f3-dad74da124d3">

## RESULT
Thus an SQL query is implemented to show record from one table that another table does not have.
