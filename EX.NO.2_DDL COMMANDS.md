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
### 1) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY: 
```
CREATE TABLE student (
    RegisterNumber INT PRIMARY KEY,
    Name VARCHAR2(50),
    Age INT,
    Address VARCHAR2(100),
    PhoneNumber VARCHAR2(20)
);
```
### OUTPUT:
![Screenshot 2024-03-20 105210](https://github.com/22003197/DBMS/assets/124332243/9eee1d1c-8805-4d10-9551-c321b67d32f2)

### 2) Alter the above student table by adding another attribute department
### SQL QUERY: 
```
ALTER TABLE student
ADD department VARCHAR2(50);
```
### OUTPUT:

![Screenshot 2024-03-20 110014](https://github.com/22003197/DBMS/assets/124332243/37b8fd05-146a-401f-b4b0-92e9a2eef15a)

### 3) Rename the student table to mystudent

### SQL QUERY: 
```
ALTER TABLE student RENAME TO mystudent;
```
### OUTPUT:
![Screenshot 2024-03-20 110014](https://github.com/22003197/DBMS/assets/124332243/7a425ba8-4809-43bd-8474-5031254689d3)

### 4) Delete the mystudent rows using truncate keyword

### SQL QUERY: 
```
TRUNCATE TABLE mystudent;
```
### OUTPUT:
![Screenshot 2024-03-20 110237](https://github.com/22003197/DBMS/assets/124332243/bcf26fd5-dff7-4fce-8ad0-a98235ad0a7c)

### 5) Drop the mystudent table
 
### SQL QUERY: 
```
DROP TABLE mystudent;
```
### OUTPUT:

![image](https://github.com/22003197/DBMS/assets/124332243/7cf06db0-db2e-4220-8c62-379cbcf0f7ff)
## Result:
         Thus the basic DDL commands in SQL are executed. 


