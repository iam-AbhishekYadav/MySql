# MySql

# # Clauses in SQL

## 1. Where Clause

- To define some conditions.
- The WHERE clause is used to filter records.
- **Syntax** :
``` mysql
SELECT col1, col2
FROM table_name 
WHERE conditions;
```

## Operators in Where Clause

**1. `Arithemtic Operator`** ---> +, -, *, /, %  
**2. `Comparision Operator`** ---> =, !=, >, >=, <, <=  
**3. `Logical Operator`** ---> AND, OR, NOT, BETWEEN, ALL, LIKE, ANY  
**4. `Bitwise Operator`** ---> &( Bitwise AND), | (Bitwise OR)  

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


select * from student                           
where marks between 80 and 90;                             # Shows marks beteen 80 to 90

select * from student
where city in ("delhi", "mumbai");                         # Shows data with city delhi, mumbai

select * from student
where city not in ("delhi", "mumbai");                     # Shows data without city delhi, mumbai
```

## 2. Limite Clause

- Sets an upper limit on numbre of (tuple) rows to be returned
- **Syntax** :
```
SELECT col1, col2
FROM table_name
LIMIT number;
```
## 3. Order By Clause

- To sort data in ascendind order (ACS) or decending order (DESC)
- **Syntax** :
```
SELECT col1, col2
FROM table_name
ORDER NY col_name(s) ASC/DESC;
```

## 4. Group By Clause

- Groups rows that have the same values into summary rows.
- It collects data from multiple record and groups the result by one or more column.
- Generally we use group by with some `Aggregation Function`.
- **Syntax** :
```
SELECT col1, col2, AGGREGATE_FUNCTION(column_name)
FROM table_name
GROUP BY col1, col2
```

## 5. Having Clause

- Similar to Where clause i.e applies some conditions on rows.
- It is used when we want to apply any condition after grouping.
- **Syntax** :
```
SELECT column_name, AGGREGATE_FUNCTION(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

# # General Order

``` mysql
SELECT column(s)  
FROM table_name  
WHERE condition  
GROUP BY column(s)  
HAVING condition  
ORDER BY column(s) ASC ;
```

# # Aggregate Function

- Aggregate Function perform a calculation on a set of values, and return a single value
- Commonly Used SQL Aggregate Functions
  - **`Count()`** ---> Counts the number of rows
  - **`Sum()`** --->  Calculates the total sum of a numeric column.
  - **`Avg()`** ---> Calculates the average of a numeric column.
  - **`Max()`** ---> Returns the Largest value from a column.
  - **`Min()`** ---> Returns the Smallestvalue from a column.
  - **`First()`** ---> Returns the first value in an ordered set of values.
  - **`Last()`** ---> Returns the last value in an ordered set of values.
- **Syntax** :
```
SELECT col1, col2, AGGREGATE_FUNCTION(column_name)
FROM table_name ;
```

## Example ---> 

``` musql
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


select count(rollno)             # Output : 6
from student;

select min(marks)                # Output : 12
from student;
``` 

























