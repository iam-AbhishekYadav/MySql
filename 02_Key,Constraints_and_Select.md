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

# # Select in SQL

- It is used to select any data from the database.
- **Syntax** :
  - **Basics Syntax** ---> `SELECT col1,col2 FROM table_name;`
  - **To Select All** ---> `SELECT * FROM table_name;`

### Example --->

``` mysql
create database school;
use school;

create table student (
	rollno int primary key,
	name varchar(50),
	marks int not null,
	grade varchar(1),
	city varchar(20)
);

insert into Student
	(rollno, name, marks, grade, city)
values
	(101, "anil", 78, "C", "Pune"),
	(102, "bhumika", 93, "A", "Mumbai"),
	(103, "chetan", 85, "B", "Mumbai"),
	(104, "dhruv", 96, "A", "Delhi"),
	(105, "emanuel", 12, "F", "Delhi"),
	(106, "farah", 82, "B", "Delhi");


select city from student;                        # Shows all city in table
select distinct city from student;               # Shows Non Duplicate vales (city)
select * from student;                           # Shows all table
```



































