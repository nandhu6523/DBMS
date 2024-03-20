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
 create table student(rollno int,name char(20),age int,address varchar(20),phoneno int);


### OUTPUT:
   ![Screenshot 2024-03-20 105305](https://github.com/nandhu6523/DBMS/assets/123856724/32f888d5-6f11-4374-8338-e319ef933b97)


### 2) Alter the above student table by adding another attribute department

### SQL QUERY: 

alter table student add department char(30);

### OUTPUT:
  ![Screenshot 2024-03-20 105401](https://github.com/nandhu6523/DBMS/assets/123856724/84a2b844-6df6-41a3-a129-f1f847cae16a)


### 3) Rename the student table to mystudent

### SQL QUERY:
drop table student;



### OUTPUT:
  ![Screenshot 2024-03-20 105830](https://github.com/nandhu6523/DBMS/assets/123856724/1ad35aef-48de-446d-a4e0-6e1eff76c77f)


### 4) Delete the mystudent rows using truncate keyword

### SQL QUERY: 
truncate table student;


### OUTPUT:

  ![Screenshot 2024-03-20 105830](https://github.com/nandhu6523/DBMS/assets/123856724/d8c86dbb-33c1-483a-8bf8-34162ae02c23)

### 5) Drop the mystudent table
 
### SQL QUERY: 
alter table student rename to mystudent;


### OUTPUT:

 ![Screenshot 2024-03-20 110019](https://github.com/nandhu6523/DBMS/assets/123856724/2743f080-5336-4a12-9ce7-1267fed478de)









## Result:
         Thus the basic DDL commands in SQL are executed. 


