# EXP NO 1: ER DIAGRAM CREATION, RELATIONAL MODEL AND SCHEMA GENERATION  
### DATE
## AIM:
<div align="justify">
   To create a ER Diagram for Bank management system or College management system using ERD Plus tool and generate the relational model with schema. 
</div>

## Algorithm
1. Create a login with https://erdplus.com.
2. Create a new ER Diagram with name
3. Create a strong entity, relation and attributes.
4. Create a weak entity, relation and attributes.
5. Specify attributes unique, multivalued and composite attributes.

### ER Diagram 

![Screenshot 2024-03-13 103729](https://github.com/Jashwanafathima/DBMS/assets/119560192/7b17223b-ed56-42eb-a9b2-0f4d175df2e4)

### Relational model
![Screenshot 2024-03-13 103756](https://github.com/Jashwanafathima/DBMS/assets/119560192/aaa80193-b9bf-4b8e-84f8-a1b358ee8120)


### SQL DDL Schema 
```
CREATE TABLE BANK
(
  Code INT NOT NULL,
  Name INT NOT NULL,
  Addr INT NOT NULL,
  PRIMARY KEY (Code)
);

CREATE TABLE BANK_BRANCH
(
  Branch_no INT NOT NULL,
  Addr INT NOT NULL,
  PRIMARY KEY (Branch_no)
);

CREATE TABLE LOAN
(
  Loan_no INT NOT NULL,
  Amount INT NOT NULL,
  Type INT NOT NULL,
  PRIMARY KEY (Loan_no)
);

CREATE TABLE CUSTOMER
(
  Phone INT NOT NULL,
  Ssn INT NOT NULL,
  Name INT NOT NULL,
  Addr INT NOT NULL,
  PRIMARY KEY (Ssn)
);

CREATE TABLE ACCOUNT
(
  Acct_no INT NOT NULL,
  Balance INT NOT NULL,
  Type INT NOT NULL,
  PRIMARY KEY (Acct_no)
);
```
## RESULT 
<div align="justify">
Thus the ER diagram was drawn and relational diagram, SQL DDL staements are generated using ERD plus tool.
</div>
