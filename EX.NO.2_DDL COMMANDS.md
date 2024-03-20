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
 `create table student(rollno int,name char(20),age int,address varchar(20),phoneno int);`


### OUTPUT:
   ![Screenshot 2024-03-20 105305](https://github.com/nandhu6523/DBMS/assets/123856724/32f888d5-6f11-4374-8338-e319ef933b97)


### 2) Alter the above student table by adding another attribute department

### SQL QUERY: 

`alter table student add department char(30);`

### OUTPUT:
  ![Screenshot 2024-03-20 105401](https://github.com/nandhu6523/DBMS/assets/123856724/84a2b844-6df6-41a3-a129-f1f847cae16a)


### 3) Rename the student table to mystudent

### SQL QUERY:
`alter table student rename to mystudent;`



### OUTPUT:
![Screenshot 2024-03-20 110019](https://github.com/nandhu6523/DBMS/assets/123856724/3472d823-ecc5-4ae3-ab58-042383240764)




### 4) Delete the mystudent rows using truncate keyword

### SQL QUERY: 
`truncate table student;`


### OUTPUT:

![Screenshot 2024-03-20 105953](https://github.com/nandhu6523/DBMS/assets/123856724/2bfe15d5-6ed6-4e49-b474-abbb6c7a8e4f)


### 5) Drop the mystudent table
 
### SQL QUERY: 
`alter table student rename to mystudent;`


### OUTPUT:

![Screenshot 2024-03-20 105830](https://github.com/nandhu6523/DBMS/assets/123856724/8333d457-8fca-4466-9c4e-649a858ed20d)










## Result:
         Thus the basic DDL commands in SQL are executed. 


