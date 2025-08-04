# # MySql

# # Databases

- Databases is a collection od data in a format that can be easily accessed (Digital).
- It allows users and applications to easily access, update, and manipulate information.
- Databases are managed using specialized software known as a Database Management System (DBMS).
- DBMS facilitates the storage, retrieval, and manipulation of data.

## Types of Databases

# # What is SQL

- SQL is a programming language used to interact with relational databases.
- SQL is declarative programming language.
- It allows users to store, retrieve, update, and manage data efficiently through simple commands.
- It is used to perform CURD operations:
  - Create
  - Read
  - Update
  - Delete

# # How to open MySql Console ??

- Open Command Prompt (CMD)
- Type **`mysql -u root -p`**
  - `-u` ---> User Name (root)
  - `-p` ---> Password

``` sql
C:\Users\mail4> mysql -u root -p                                            # User Name = root
Enter password: ****                                                        # Password = 1354
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 22
Server version: 9.4.0 MySQL Community Server - GPL

Copyright (c) 2000, 2025, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql>
```
# # Some SQL Commands

**1. `CREATE DATABASE db_name ;`** ---> To Create Database  
**2. `CREATE DATABASE IF NOT EXSIST db_name ;`** ---> To Create database if database is not exist  
**3. `DROP DATABASE db_name ;`** ---> To Delete Database  
**4. `DROP DATABASE IF EXISTS db_name ;`** ---> To Delete database if database is exist  
**5. `SHOW DATABASE ;`** ---> To Show lists of all Database  
**6. `USE db_name ;`** ---> To select/use a specific database  

# # SQL Data Types

In SQL, data types define the kind of data that can be stored in a column or variables.

<img src="https://github.com/user-attachments/assets/e5779e10-f972-44b4-bc89-52e2a6bc671a" width="600" height="700">

> [!NOTE]
> CHAR is for fixed length & VARCHAR is for variable length strings. Generally,
VARCHAR is better as it only occupies necessary memory & works more efficiently.

# # Tables in SQL

The CREATE TABLE statement is used to create a new table in a database.

### Syntax

``` sql
CREATE TABLE table_name (  
    column1 datatype,  
    column2 datatype,  
    column3 datatype,  
   ....  
);
```

### Command used to make Table Database.

**1. `create table tb_name ;`** ---> To create table in database  
**2. `use db_name ;`** ---> To select a specific database  
**3. `show tables ;`** ---> To Show tables in database  
**4. `Insert`** ---> To insert values in database 

``` mysql
INSER INTO table_name
(column_name_1, column_name_2)
VALUES
(col1_v1, col1_v2),
(col2_v1, col2_v2);
````
**5. `select * from tb_name ;`** ---> To print/view table from database (* --> All)    

``` mysql
mysql> create database Movies_Database;
Query OK, 1 row affected (0.079 sec)

mysql> use Movies_Database;
Database changed
mysql> create table Movies (Name VARCHAR(100),Rating INTEGER);
Query OK, 0 rows affected (0.223 sec)

mysql> show tables;
+------------------+
| Tables_in_movies |
+------------------+
| movies           |
+------------------+
1 row in set (0.019 sec)

mysql> insert into movies (Name, Rating) values ("Avenges Infinity War", 5);
Query OK, 1 row affected (0.087 sec)

mysql> insert into movies (Name, Rating) values ("Iron Man", 4);
Query OK, 1 row affected (0.061 sec)

mysql> insert into movies (Name, Rating) values ("Spider Man", 4);
Query OK, 1 row affected (0.239 sec)

mysql> select * from movies;
+----------------------+--------+
| Name                 | Rating |
+----------------------+--------+
| Avenges Infinity War |      5 |
| Iron Man             |      4 |
| Spider Man           |      4 |
+----------------------+--------+
3 rows in set (0.006 sec)

mysql>
```








