# # MySql

# # Keys in SQL

## Primary Key :

- It is column (or set of columns) in a table that uniquely identifies each row.
- There is only 1 Primary Key (A unique Id).
- It should be NOT null.

## Foreign Key

- A foreign key is a column (or set of columns) in a table that refers to the primary key
- There can be multiple Foreign Keys.
- Foreign Key have duplicate & null values.  

### Example :
 
**`id`** --> Primary Key   
**`cityid`** --> Foreign Key

<img src="https://github.com/user-attachments/assets/b245b2ae-58c5-4e2e-9ab7-627c6b2a4092" width="600" height="500">

# # Constraints in SQL

SQL constraints are used to specify rules for data in a table.

### Some Popular Constraints

**1 `NOT NULL`**
- Columns cannot have a null value
- **Syntax** : `col_1 int NOT NULL`

**2 `UNIQUE`**

- All values in column are different.
- **Syntax** : `col_1 int UNIQUE`

**3 `PRIMARY KEY`**

- Makes a column unique & not null but used only for one
- **Syntax** :
  - `id int PRIMARY KEY`
  - ```
    CREATE TABLE temp (
          id INT ,
          name VARCHAR(50),
          city VARCHAR(20),
          PRIMARY KEY (id, name)
     );
    ```
    
**4 `FOREIGN KEY`**

- Prevent actions that would destory links between tables.
- **Syntax** :
```
CREATE TABLE temp (
 cust_id int,
 FOREIGN KEY (cust_id) references customer(id)
);
```

**5 `DEFAULT`**

- Sets the default value of a column
- **Syntax** : `salary INT DEFAULT 2500`


**6 `Check`**

- It can limit the values allowed in a column
- **Syntax** : 
```
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype CHECK (condition),
    ...
);
```






































