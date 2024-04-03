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
    employee_id INT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    department VARCHAR(50),
    salary DECIMAL(10, 2)
);
INSERT INTO EMPLOYEE (employee_id, first_name, last_name, department, salary)
VALUES (1, 'John', 'Doe', 'IT', 60000.00);

INSERT INTO EMPLOYEE (employee_id, first_name, last_name, department, salary)
VALUES (2, 'Jane', 'Smith', 'HR', 55000.00);
```
### OUTPUT:
![Screenshot 2024-04-03 102324](https://github.com/nandhu6523/DBMS/assets/123856724/60705640-4b6f-4c64-bcd6-182485174857)

### 2) Create a synonym S1 for EMPLOYEE  table.

### SQL QUERY: 
```
CREATE SYNONYM S1 FOR EMPLOYEE;
```
### OUTPUT:
![Screenshot 2024-04-03 102406](https://github.com/nandhu6523/DBMS/assets/123856724/e18ffd12-5392-456a-b774-61ce65b46db2)

### 3) Display the EMPLOYEE  table using synonym S1.
 
### SQL QUERY: 
```
SELECT * FROM S1;
```
### OUTPUT:
![Screenshot 2024-04-03 102429](https://github.com/nandhu6523/DBMS/assets/123856724/3c81fb5c-ebd0-4f3f-838b-928ff51827bf)

### 4) Drop the synonym.

### SQL QUERY: 
```
DROP SYNONYM S1;
```
### OUTPUT:
![Screenshot 2024-04-03 102454](https://github.com/nandhu6523/DBMS/assets/123856724/1258ffde-3e9f-43da-b320-d9406845bde2)

### 5) Create a supplier table and create a sequence S2 for supplier table id.

### SQL QUERY: 
```
CREATE SEQUENCE S2 START WITH 1 INCREMENT BY 1;
CREATE TABLE SUPPLIER (
    id INT PRIMARY KEY,
    supplier_name VARCHAR(100),
    contact_name VARCHAR(100),
    address VARCHAR(255),
    city VARCHAR(100),
    state VARCHAR(100),
    postal_code VARCHAR(20),
    country VARCHAR(100)
);
```
### OUTPUT:
![Screenshot 2024-04-03 102619](https://github.com/nandhu6523/DBMS/assets/123856724/33d326f7-ba40-4f20-bd10-862af854638d)
### 6) insert the data into supplier table use sequence.

### SQL QUERY: 
```
INSERT INTO SUPPLIER (id, supplier_name, contact_name, address, city, state, postal_code, country)
VALUES (S2.NEXTVAL, 'ABC Suppliers', 'John Doe', '123 Main Street', 'New York', 'NY', '10001', 'USA');

INSERT INTO SUPPLIER (id, supplier_name, contact_name, address, city, state, postal_code, country)
VALUES (S2.NEXTVAL, 'XYZ Corporation', 'Jane Smith', '456 Elm Street', 'Los Angeles', 'CA', '90001', 'USA');
```
### OUTPUT:
![Screenshot 2024-04-03 102644](https://github.com/nandhu6523/DBMS/assets/123856724/31ccd4c9-2d11-428b-98d2-77fe7f198274)
### 7) Drop the sequence

### SQL QUERY: 
```
DROP SEQUENCE S2;
```
### OUTPUT:
![Screenshot 2024-04-03 102706](https://github.com/nandhu6523/DBMS/assets/123856724/a4f435da-1476-4608-a8bb-a3f15afba678)
## RESULT :
### Thus the sequence and synonym created and used in SQL.
