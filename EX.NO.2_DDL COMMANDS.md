# EXP NO 2: DATA DEFINITION LANGUGE COMMANDS 
### DATE
## AIM:
To create a student database and execute DDL queries using SQL.


## THEORY
### DDL (Data Definition Language)

* DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema.
* It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.
* DDL is a set of SQL commands used to create, modify, and delete database structures but not data.
* These commands are normally not used by a general user, who should be accessing the database via an application.

 
### List of DDL commands: 
1. CREATE: This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).
2. DROP: This command is used to delete objects from the database.
3. ALTER: This is used to alter the structure of the database.
4. TRUNCATE: This is used to remove all records from a table, including all spaces allocated for the records are removed.
5. RENAME: This is used to rename an object existing in the database.

## Query:
### 1) Create a database studentdb

### SQL QUERY:
```
create database studentdbb;
```
### OUTPUT:
![Screenshot 2024-03-13 110901](https://github.com/Jashwanafathima/DBMS/assets/119560192/a13014c8-7ee2-4270-bef1-88011aa539e7)
![Screenshot 2024-03-13 110941](https://github.com/Jashwanafathima/DBMS/assets/119560192/8a3a401c-4d82-44bd-8a7a-04c4e9180d59)

### 2) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY: 
```
create table student(RegisterNumber int,Name varchar(100),Age int,Address varchar(250),PhoneNumber int) ;
```

### OUTPUT:
![Screenshot 2024-03-13 111253](https://github.com/Jashwanafathima/DBMS/assets/119560192/bd4e7c8d-dc53-4d07-92fc-d3c12fccf5eb)

### 3) Alter the above student table by adding another attribute department

### SQL QUERY: 
```
 alter table student add dept varchar(20);
```
### OUTPUT:
![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/ade198ea-a1e0-490f-8732-d5d0f116169f)

### 4) Rename the student table to mystudent

### SQL QUERY: 
```
rename table student to mystudent;
```

### OUTPUT:
![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/e7f1fd2e-2f43-49b1-b557-35fb4c39b956)


### 5) Delete the mystudent rows using truncate keyword

### SQL QUERY: 
```
truncate table mystudent;
```

### OUTPUT:

![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/78effdfa-3c00-47cf-a4cd-4eec1d8b6c19)

### 6) Drop the mystudent table
 
### SQL QUERY: 

```
drop table mystudent;
```
### OUTPUT:

![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/86a59dc0-26de-4e22-a7cb-59c3cd3cdcca)


## Result:
         Thus the basic DDL commands in SQL are executed. 


