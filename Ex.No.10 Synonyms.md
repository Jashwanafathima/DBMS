# EXP NO 10: SYNONYMS AND ASSERTIONS IN SQL 
### DATE: 
## AIM:
To create a student database and create a synonym and assertions.

## THEORY
## SYNONYM
<div align="justify">
A SYNONYM provides another name for database object, referred to as original object, that may exist on a local or another server.
</div>
## ASSERTIONS
<div align="justify">
* An assertion is a piece of SQL which makes sure a condition is satisfied, else or it stops the action being taken on a database.
* An assertion is a constraint that might be dependent upon multiple rows of multiple tables.
</div>

## Query:
### 1) Create a table EMPLOYEE and perform insertion of two rows.

### SQL QUERY: 
```
CREATE TABLE EMPLOYEE (
    employee_id INT ,
    name VARCHAR(255),
    department VARCHAR(255),
    salary DECIMAL(10, 2)
);
```

### OUTPUT:

### 2) Create a synonym S1 for EMPLOYEE  table.

### SQL QUERY: 
```
CREATE SYNONYM S1 FOR EMPLOYEE;
```
### OUTPUT:


### 3) Display the EMPLOYEE  table using synonym S1.
 
### SQL QUERY: 
```
SELECT * FROM S1;
```

### OUTPUT:


### 4) Drop the synonym.

### SQL QUERY: 
```
DROP SYNONYM S1;
```

### OUTPUT:



### 5) Create a supplier table and create a sequence S2 for supplier table id.

### SQL QUERY: 
```
CREATE TABLE supplier (
    id INT,
    name VARCHAR(255),
    address VARCHAR(255),
    contact_person VARCHAR(255)
);

CREATE SEQUENCE S2 START 1;

```

### OUTPUT:


### 6) insert the data into supplier table use sequence.

### SQL QUERY: 
```
INSERT INTO supplier (id, name, address, contact_person)
VALUES (NEXTVAL('S2'), 'ABC Suppliers', '123 Main Street', 'John Doe');

INSERT INTO supplier (id, name, address, contact_person)
VALUES (NEXTVAL('S2'), 'XYZ Distributors', '456 Elm Road', 'Jane Smith');
```

### OUTPUT:
### 7) Drop the sequence

### SQL QUERY: 
```
DROP SEQUENCE S2;
```

### OUTPUT:

### RESULT:
Thus the sequence and synonym created and used in SQL.


## RESULT :
### Thus the sequence and synonym created and used in SQL.
