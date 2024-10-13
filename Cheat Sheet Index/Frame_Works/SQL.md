# SQL Server Cheat Sheet

## 1. **Basic SQL Syntax**

| Command                | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **SELECT**             | Retrieve data from a table.                  | ```sql SELECT * FROM Users; ```       |
| **WHERE**              | Filter results based on conditions.           | ```sql SELECT * FROM Users WHERE age > 30; ``` |
| **ORDER BY**           | Sort the result set.                          | ```sql SELECT * FROM Users ORDER BY name ASC; ``` |
| **GROUP BY**           | Group rows sharing a property.                | ```sql SELECT COUNT(*) FROM Users GROUP BY country; ``` |
| **HAVING**             | Filter grouped results.                        | ```sql SELECT country, COUNT(*) FROM Users GROUP BY country HAVING COUNT(*) > 5; ``` |

---

## 2. **Data Manipulation Commands**

| Command                | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **INSERT**             | Add new records to a table.                  | ```sql INSERT INTO Users (name, age) VALUES ('John', 30); ``` |
| **UPDATE**             | Modify existing records.                      | ```sql UPDATE Users SET age = 31 WHERE name = 'John'; ``` |
| **DELETE**             | Remove records from a table.                 | ```sql DELETE FROM Users WHERE name = 'John'; ``` |

---

## 3. **Creating and Managing Tables**

| Command                | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **CREATE TABLE**       | Create a new table.                          | ```sql CREATE TABLE Users (id INT PRIMARY KEY, name NVARCHAR(100), age INT); ``` |
| **ALTER TABLE**        | Modify an existing table (add/remove columns). | ```sql ALTER TABLE Users ADD email NVARCHAR(100); ``` |
| **DROP TABLE**         | Delete a table and its data.                 | ```sql DROP TABLE Users; ```          |

---

## 4. **Constraints**

| Constraint             | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **PRIMARY KEY**        | Uniquely identifies each record in a table. | ```sql CREATE TABLE Users (id INT PRIMARY KEY, name NVARCHAR(100)); ``` |
| **FOREIGN KEY**        | Enforces a link between two tables.           | ```sql ALTER TABLE Orders ADD FOREIGN KEY (user_id) REFERENCES Users(id); ``` |
| **UNIQUE**             | Ensures all values in a column are unique.   | ```sql CREATE TABLE Users (id INT PRIMARY KEY, email NVARCHAR(100) UNIQUE); ``` |
| **CHECK**              | Ensures that all values in a column satisfy a specific condition. | ```sql CREATE TABLE Users (id INT, age INT CHECK (age >= 18)); ``` |

---

## 5. **Joins**

| Join Type              | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **INNER JOIN**         | Returns records with matching values in both tables. | ```sql SELECT Users.name, Orders.total FROM Users INNER JOIN Orders ON Users.id = Orders.user_id; ``` |
| **LEFT JOIN**          | Returns all records from the left table and matched records from the right. | ```sql SELECT Users.name, Orders.total FROM Users LEFT JOIN Orders ON Users.id = Orders.user_id; ``` |
| **RIGHT JOIN**         | Returns all records from the right table and matched records from the left. | ```sql SELECT Users.name, Orders.total FROM Users RIGHT JOIN Orders ON Users.id = Orders.user_id; ``` |
| **FULL OUTER JOIN**    | Returns all records when there is a match in either table. | ```sql SELECT Users.name, Orders.total FROM Users FULL OUTER JOIN Orders ON Users.id = Orders.user_id; ``` |

---

## 6. **Functions**

| Function                | Description                                   | Example                                |
|-------------------------|-----------------------------------------------|----------------------------------------|
| **COUNT()**             | Returns the number of rows.                  | ```sql SELECT COUNT(*) FROM Users; ``` |
| **SUM()**               | Returns the sum of a numeric column.         | ```sql SELECT SUM(age) FROM Users; ``` |
| **AVG()**               | Returns the average value of a numeric column. | ```sql SELECT AVG(age) FROM Users; ``` |
| **MIN()**               | Returns the minimum value.                    | ```sql SELECT MIN(age) FROM Users; ``` |
| **MAX()**               | Returns the maximum value.                    | ```sql SELECT MAX(age) FROM Users; ``` |

---

## 7. **Transactions**

| Command                | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **BEGIN TRANSACTION**  | Start a transaction.                         | ```sql BEGIN TRANSACTION; ```         |
| **COMMIT**             | Save changes made during the transaction.    | ```sql COMMIT; ```                     |
| **ROLLBACK**           | Undo changes made during the transaction.    | ```sql ROLLBACK; ```                   |

---

## 8. **Stored Procedures**

| Concept                | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Creating Stored Procedure** | Define reusable SQL code.               | ```sql CREATE PROCEDURE GetUsers AS SELECT * FROM Users; ``` |
| **Executing Stored Procedure** | Call a stored procedure.                | ```sql EXEC GetUsers; ```              |
| **Parameters**         | Pass parameters to a stored procedure.        | ```sql CREATE PROCEDURE GetUserById @id INT AS SELECT * FROM Users WHERE id = @id; ``` |

---

## 9. **Views**

| Concept                | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Creating a View**    | Create a virtual table based on a query.    | ```sql CREATE VIEW UserOrders AS SELECT Users.name, Orders.total FROM Users INNER JOIN Orders ON Users.id = Orders.user_id; ``` |
| **Selecting from a View** | Query a view like a table.               | ```sql SELECT * FROM UserOrders; ```  |
| **Dropping a View**    | Remove a view from the database.            | ```sql DROP VIEW UserOrders; ```      |

---

## 10. **Indexing**

| Concept                | Description                                   | Example                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Creating an Index**  | Improve query performance by indexing columns. | ```sql CREATE INDEX idx_name ON Users(name); ``` |
| **Dropping an Index**   | Remove an index from a table.                | ```sql DROP INDEX idx_name ON Users; ``` |

---

This **SQL Server Cheat Sheet** provides a comprehensive overview of key concepts, commands, and best practices for effective database management.

Key Command
Ctrl/Cmd + B Toggle bold
Ctrl/Cmd + I Toggle italic
Alt+S (on Windows) Toggle strikethrough1
Ctrl + Shift + ] Toggle heading (uplevel)
Ctrl + Shift + [ Toggle heading (downlevel)
Ctrl/Cmd + M Toggle math environment
Alt + C Check/Uncheck task list item
Ctrl/Cmd + Shift + V Toggle preview
Ctrl/Cmd + K V Toggle preview to side