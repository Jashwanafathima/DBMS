# EX.NO 4 Data Control Language (DCL) Commands and Transaction Control Languages (TCL) in SQL
### DATE:
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## Data Control Language (DCL) commands
* Data control language (DCL) is used to access the stored data.
* It is mainly used for revoke and to grant the user the required access to a database.
## List of DCL commands: 
1. GRANT : It is used to insert data into a table.
2. REVOKE: It is used to update existing data within a table.
## Transaction control language(TCL) commands
1. COMMIT : COMMIT command in SQL is used to save all the transaction-related changes permanently to the disk
2. START TRANSACTION : to start the transaction
3. ROLLBACK : undo the transaction upto savepoint 
4. SAVEPOINT : create a savepoint to save the different parts of the same transaction using different names

### Q1) Create a table employee with employee id ,name and Address

### QUERY:
```
sql
create table employee(
emp_id numeric,
emp_name varchar(10),
addr varchar(40)
);
```

### OUTPUT:

![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/05b59355-4448-4369-b836-64c09bdccba6)



### Q2) Insert three rows into emploee table 
### QUERY:
```
insert into employee values(1,'Luffy','EastBlue');
insert into employee values(2,'Shanks','GodValley');
insert into employee values(3,'Grap','MarinFord');
```

### OUTPUT:

![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/e4bc8c74-1df9-4b2c-b3b4-04194784a8b6)

### Q3) Start the transaction and create a save point s1.

### QUERY:
```
savepoint A;
```
### OUTPUT:

![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/bd18b0bc-3753-47f9-a39a-e85df6265bb3)

### Q4) Perform insertion into employee table.

### QUERY:
```
insert into employee(4,'Robin','EniesLobby');
```

### OUTPUT:
![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/3ee38ddc-2a99-4566-9790-53b11e4889a4)


### Q5)	Display the employee table and create a save point s2 .


### QUERY:
```
sql
select * from employee;
savepoint s2;
```

### OUTPUT:
![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/23d2b8d1-fd6a-44c7-8a5c-3809b42339c5)


### Q6)	Perform updation on any one of the row.


### QUERY:
```
sql
update employee set emp_name='Nico Robin' where emp_id=4;
```

### OUTPUT:
![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/b1237ea5-e53a-4827-afa8-59b04a7e6351)


### Q7) Display the employee table and rollback to  save point s2 


### QUERY:
```
sql
select * from employee;
rollback to s2;
```

### OUTPUT:
![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/24bd3f7a-db15-4ed9-b44b-f821f1692c6c)


### Q8) Display the employee table and commit the changes; 


### QUERY:
```
sql
select * from employee;
commit;
```

### OUTPUT:
![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/344bcc56-b487-4988-a4d4-b5ba817c682d)


### Q(9) Rollback to save point s1;


### QUERY:
```
sql
rollback to A;
```

### OUTPUT:
![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/f6603b25-04ce-41b7-ae55-408dabc25857)


### Q10)	Create a new user and grant access to any one database with "insert and update"


### QUERY:
```
CREATE USER new_user;
GRANT INSERT, UPDATE ON database_name TO new_user;
```

### OUTPUT:
![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/9b798005-5a9e-46e0-bc83-1555230575dc)


### Q11) Check the user access and display the result 


### QUERY:
```
SHOW GRANTS FOR new_user;
```

### OUTPUT:
![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/fa39f5a0-a37c-448a-ad2a-5f728bf9492d)

### Q12) Revoke the privillages.

### QUERY:
```
SHOW GRANTS FOR new_user;
REVOKE INSERT, UPDATE ON database_name FROM new_user;
SHOW GRANTS FOR new_user;
```

### OUTPUT:
![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/74984fb1-40ae-4b1c-a00e-1a5c6c987b47)


## RESULT :
Thus the basic TCL and DCL commands are executed.
