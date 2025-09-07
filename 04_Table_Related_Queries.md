# # Table Related Queries

## Update Query

- It allows updating one or multiple columns, with or without conditions, to keep data accurate and consistent.
- **Syntax** :
``` mysql
UPDATE table_name  
SET column1 = value1, column2 = value2,...   
WHERE condition;  
```

#### Example ---> Updated grade 'O' where grade is 'A'

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

set SQL_SAFE_UPDATES = 0;

update student
set grade = "O"
where grade = "A";

select * from student;
```

## Delete Query

- It is used to remove specific rows from a table while keeping the table structure intact.
- It is different from DROP, which deletes the entire table.
- **Syntax** :
``` mysql
DELETE FROM table_name
WHERE some_condition;
```

## Alter Query

- It modify the structure of an existing table in a database.
- Whether adding new columns, modifying existing ones, deleting columns or renaming them.
- It enables you to make changes without losing data stored in the table.
- **Syntax** :
``` mysql
ALTER TABLE table_name
[ADD | DROP | MODIFY | RENAME | CHANGE] column_name datatype;
```
- Parameters :
  - `table_name` : Name of the table you want to modify.
  - `ADD` : Used to add a new column.
  - `DROP` : Used to remove an existing column.
  - `MODIFY` : Used to change datatype or definition of an existing column.
  - `RENAME` : Used to rename table.
  - `CHANGE` : Used to cahnge column name or datatype.


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

alter table student
add column age int not null default 19;

alter table student
drop column age ;

select * from student;
```

## Truncate Table 

- It remove all rows from a table, leaving the table structure intact.
- This operation is often favored over the DELETE statement for its efficiency, especially when dealing with large datasets.
- **Synatx** :
``` mysql
TRUNCATE TABLE table_name;
```


# # Cascading for Foreign Key

## On Delete Cascade

When we create a foreign key using this option, it deletes the referencing rows in the child table when the referenced row is deleted in the parent table which has a primary key.

## On Update Cascade

When we create a foreign key using UPDATE CASCADE the referencing rows are updated in the child table when the refrenced row is updated in the parent table which has a primary key.

## Syntax :

``` mysql
CREATE TABLE student (
id INT PRIMARY KEY ,
courseId INT ,
FOREGN KEY (courseId) REFRENCES course(id)
ON DELETE CASCADE
ON UPDATE CASCADE
);
```


































