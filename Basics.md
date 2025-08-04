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

**1. `create database db_name ;`** ---> To Create Database  
**2. `drop database db_name ;`** ---> To Delete Database  
**3. `show database ;`** ---> To Show lists of all Database  
**3. `show db_name ;`** ---> To select a specific database  

# # SQL Data Types

In SQL, data types define the kind of data that can be stored in a column or variables.

<img src="https://github.com/user-attachments/assets/e5779e10-f972-44b4-bc89-52e2a6bc671a" width="600" height="700">

> [!NOTE]
> CHAR is for fixed length & VARCHAR is for variable length strings. Generally,
VARCHAR is better as it only occupies necessary memory & works more efficiently.








