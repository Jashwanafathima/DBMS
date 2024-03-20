# EX 3 Data Manipulation Language (DML) Commands and built in functions in SQL
## DATE:
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## DML(Data Manipulation Language)
*  The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements.
*  It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.

## List of DML commands: 
1. INSERT: It is used to insert data into a table.
2. UPDATE: It is used to update existing data within a table.
3. DELETE: It is used to delete records from a database table.
4. SELECT: The SELECT command shows the records of the specified table.

## Create the table as given below:
```sql
create table manager(enumber number(6),ename char(15),salary number(5),commission number(4),annualsalary number(7),Hiredate date,designation char(10),deptno number(2),reporting char(10));
```
## insert the following values into the table
```sql
insert into manager values(7369,'Dharsan',2500,500,30000,'30-June-81','clerk',10,'John');
insert into manager values(7839,'Subu',3000,400,36000,'1-Jul-82','manager',null,'James');
insert into manager values(7934,'Aadhi',3500,300,42000,'1-May-82','manager',30,NULL);
insert into manager values(7788,'Vikash',4000,0,48000,'12-Aug-82','clerk',50,'Bond');
```

### Q1) Update all the records of manager table by increasing 10% of their salary as bonus.

### QUERY:
```
update manager set salary=salary+(salary*0.10);
```

### OUTPUT:
![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/7ceb3431-bb37-4564-b9e1-a380e8ed2d8d)


### Q2) Delete the records from manager table where the salary less than 2750.


### QUERY:
```
delete from manager where salary<2750;
```

### OUTPUT:

![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/3001592a-0961-4c03-8977-9c6651c002c1)

### Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)


### QUERY:
```
select ename as "Name",salary*12 as "Annual salary" from manager;
```


### OUTPUT:

![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/3985f2d4-3f64-4f42-9a24-d8048c1ac083)

### Q5)	List the names of Clerks from emp table.


### QUERY:
```
select ename from manager where designation='clerk';
```


### OUTPUT:
![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/c004e7af-e09d-427c-9d28-71f21d08691b)


### Q6)	List the names of employee who are not Managers.


### QUERY:
```
select ename from manager where designation <> 'manager';
```



### OUTPUT:
![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/ed6efbaf-9217-49de-9d6d-2dad415dcc68)


### Q7)	List the names of employees not eligible for commission.


### QUERY:
```
select ename from manager where commission=0;
```

### OUTPUT:

![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/3d58ed3f-df0e-4a40-98c5-e0ad1ab1affb)

### Q8)	List employees whose name either start or end with ‘s’.


### QUERY:
```
select ename from manager where ename like '%s' or ename like 's%';
```

### OUTPUT:
![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/3a605463-7b89-43ed-8bde-85c4f4366bd1)


### Q9) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.


### QUERY:
```
select ename,designation as "job",deptno,hiredate from manager order by hiredate asc;
```

### OUTPUT:

![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/11519a1f-557c-4f2e-867d-fb897f66fe1c)

### Q10) List the Details of Employees who have joined before 30 Sept 81.


### QUERY:
```
select * from manager where hiredate<str_to_date('1981-09-30','YYYY-MM-DD');
```


### OUTPUT:

![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/74f1e5ac-8d69-45ca-a3a3-4f894d5f3eb0)

### Q11)	List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.


### QUERY:
```
 select ename,deptno,salary from manager order by deptno asc,salary desc;
```


### OUTPUT:

![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/615cf4a6-6219-4701-87d9-ca91e482a320)


### Q12) List the names of employees not belonging to dept no 30,40 & 10


### QUERY:
```
select ename from manager where deptno not in (30,40,10);
```


### OUTPUT:

![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/c5d0a430-8cc9-4d83-ab5c-82f9e0d5d7d6)

### Q13) Find number of rows in the table EMP

### QUERY:
```
 select count(*) from manager;
```

### OUTPUT:
![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/3f9e4787-87b0-4627-a65a-9d205e6239d7)


### Q14) Find maximum, minimum and average salary in EMP table.

### QUERY:
```
select max(salary) as MAX,min(salary) as MIN, avg(salary) as AVG from manager;
```

### OUTPUT:

![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/7066e7b1-5518-41f3-a019-01453842ae2b)

### Q15) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

### QUERY:
```
SELECT designation AS job, COUNT(*) AS num_employees FROM manager GROUP BY designation ORDER BY num_employees DESC;
```

### OUTPUT:
![image](https://github.com/Jashwanafathima/DBMS/assets/119560192/3a922720-897e-4108-8d85-42687b2d317e)


## RESULT :
Thus the basic DML commands are executed
