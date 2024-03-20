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

### OUTPUT:

### 2) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY: 
'''
CREATE TABLE student (
    RegisterNumber INT PRIMARY KEY,
    Name VARCHAR2(50),
    Age INT,
    Address VARCHAR2(100),
    PhoneNumber VARCHAR2(20)
);
'''

### OUTPUT:
![Screenshot 2024-03-20 105210](https://github.com/22003197/DBMS/assets/124332243/9eee1d1c-8805-4d10-9551-c321b67d32f2)

### 3) Alter the above student table by adding another attribute department

### SQL QUERY: 

### OUTPUT:

### 4) Rename the student table to mystudent

### SQL QUERY: 



### OUTPUT:

### 5) Delete the mystudent rows using truncate keyword

### SQL QUERY: 


### OUTPUT:
### 4) Drop the mystudent table
 
### SQL QUERY: 


### OUTPUT:








## Result:
         Thus the basic DDL commands in SQL are executed. 


