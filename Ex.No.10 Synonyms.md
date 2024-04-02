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
![Screenshot 2024-04-02 211604](https://github.com/22003197/DBMS/assets/124332243/b5afb45d-9f47-444a-9816-6907bd75fedc)

### 2) Create a synonym S1 for EMPLOYEE  table.

### SQL QUERY: 
```
CREATE SYNONYM S1 FOR EMPLOYEE;
```
### OUTPUT:
![Screenshot 2024-04-02 211947](https://github.com/22003197/DBMS/assets/124332243/7d7602c2-a849-4c87-a8b4-690002679983)

### 3) Display the EMPLOYEE  table using synonym S1.
 
### SQL QUERY: 
```
SELECT * FROM S1;
```
### OUTPUT:
![Screenshot 2024-04-02 212043](https://github.com/22003197/DBMS/assets/124332243/d3c6feb5-c83b-4250-8f20-49fb724aa4b1)

### 4) Drop the synonym.

### SQL QUERY: 
```
DROP SYNONYM S1;
```
### OUTPUT:
![Screenshot 2024-04-02 212253](https://github.com/22003197/DBMS/assets/124332243/41752394-705a-4d0d-91f6-d89a457543ec)

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
![Screenshot 2024-04-02 212702](https://github.com/22003197/DBMS/assets/124332243/5d4ccb06-9193-41e1-a24c-ff75a02785ed)


### 6) insert the data into supplier table use sequence.

### SQL QUERY: 
```
INSERT INTO SUPPLIER (id, supplier_name, contact_name, address, city, state, postal_code, country)
VALUES (S2.NEXTVAL, 'ABC Suppliers', 'John Doe', '123 Main Street', 'New York', 'NY', '10001', 'USA');

INSERT INTO SUPPLIER (id, supplier_name, contact_name, address, city, state, postal_code, country)
VALUES (S2.NEXTVAL, 'XYZ Corporation', 'Jane Smith', '456 Elm Street', 'Los Angeles', 'CA', '90001', 'USA');
```
### OUTPUT:
![Screenshot 2024-04-02 212931](https://github.com/22003197/DBMS/assets/124332243/408c3934-a585-4f0e-803a-a9c37cfab157)

### 7) Drop the sequence

### SQL QUERY: 
```
DROP SEQUENCE S2;
```
### OUTPUT:
![Screenshot 2024-04-02 213045](https://github.com/22003197/DBMS/assets/124332243/b179d828-8cec-405d-9e29-279f0fbf3ce8)

## RESULT :
### Thus the sequence and synonym created and used in SQL.
