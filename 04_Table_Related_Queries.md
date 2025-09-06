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







