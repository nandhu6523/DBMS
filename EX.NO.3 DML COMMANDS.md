# EX 2 Data Manipulation Language (DML) Commands and built in functions in SQL
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
 UPDATE manager
 SET salary = salary * 1.1;


### OUTPUT:
![Screenshot 2024-04-02 220957](https://github.com/nandhu6523/DBMS/assets/123856724/ee6980b0-6eb7-4613-a1c2-d6437d263eca)


### Q2) Delete the records from manager table where the salary less than 2750.


### QUERY:
 DELETE FROM manager
 WHERE salary < 2750;


### OUTPUT:
![Screenshot 2024-04-02 221025](https://github.com/nandhu6523/DBMS/assets/123856724/f4875fd9-cead-4bcf-af43-df69dd709060)


### Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)


### QUERY:
SELECT ename AS "Name", salary * 12 AS "Annual Salary"
FROM manager;


### OUTPUT:
![Screenshot 2024-04-02 221120](https://github.com/nandhu6523/DBMS/assets/123856724/22320a7e-74f0-4326-afe5-105a75da8594)


### Q5)	List the names of Clerks from emp table.


### QUERY:
select ename from manager where designation = 'clerk';


### OUTPUT:
![Screenshot 2024-04-02 221239](https://github.com/nandhu6523/DBMS/assets/123856724/4923d58f-9bf3-4b65-923a-7a7ce2a7feea)



### Q6)	List the names of employee who are not Managers.


### QUERY:
select ename from manager where designation != 'manager';



### OUTPUT:
![Screenshot 2024-04-02 221239](https://github.com/nandhu6523/DBMS/assets/123856724/0e76da10-2753-47d7-adc7-3f287034af52)



### Q7)	List the names of employees not eligible for commission.


### QUERY:
select ename from manager where commission = 0;


### OUTPUT:
![Screenshot 2024-04-02 221427](https://github.com/nandhu6523/DBMS/assets/123856724/87a99f62-2aa6-484b-9a8c-c0ad33b88bda)



### Q8)	List employees whose name either start or end with ‘s’.


### QUERY:
select ename from manager where ename like 'S%' or ename like '%S';


### OUTPUT:

![Screenshot 2024-04-02 221451](https://github.com/nandhu6523/DBMS/assets/123856724/b9f060db-54f8-4b4c-8ddc-546869665e43)



### Q9) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.


### QUERY:
select Hiredate,ename,designation,deptno from manager order by Hiredate;


### OUTPUT:

![Screenshot 2024-04-02 221624](https://github.com/nandhu6523/DBMS/assets/123856724/549f5672-b3a8-475e-a77e-f3aed9fa659a)



### Q10) List the Details of Employees who have joined before 30 Sept 81.


### QUERY:
select * from manager where hiredate<to_date('1981-09-30','YYYY-MM-DD');


### OUTPUT:

![Screenshot 2024-04-02 221703](https://github.com/nandhu6523/DBMS/assets/123856724/f1d771e0-94da-47ec-9da9-c601b31ea5d1)



### Q11)	List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.


### QUERY:
select ename,deptno,salary from manager order by deptno,salary desc;


### OUTPUT:

![Screenshot 2024-04-02 221738](https://github.com/nandhu6523/DBMS/assets/123856724/b15245e4-7822-46ff-83a4-0630c62321fb)



### Q12) List the names of employees not belonging to dept no 30,40 & 10


### QUERY:
select ename from manager where deptno != 30 and deptno != 40 and deptno != 10;


### OUTPUT:


![Screenshot 2024-04-02 221810](https://github.com/nandhu6523/DBMS/assets/123856724/b978010e-416c-45c4-bc7d-f604da130fd0)


### Q13) Find number of rows in the table EMP

### QUERY:
select count (*) as count_ename from manager;


### OUTPUT:

![Screenshot 2024-04-02 221853](https://github.com/nandhu6523/DBMS/assets/123856724/9a922af8-3e63-4330-87dd-81f2a98df3b3)



### Q14) Find maximum, minimum and average salary in EMP table.

### QUERY:
select avg(salary) as tot_salary from manager;
select min(salary) as min_salary from manager;
select max(salary) as max_salary from manager;


### OUTPUT:

![Screenshot 2024-04-02 222026](https://github.com/nandhu6523/DBMS/assets/123856724/94f40b04-0978-45c2-946d-b824f9500230)

![Screenshot 2024-04-02 222031](https://github.com/nandhu6523/DBMS/assets/123856724/f39e48c7-d5c0-4891-a368-43e71c89f4e2)


![Screenshot 2024-04-02 222036](https://github.com/nandhu6523/DBMS/assets/123856724/fc9d8f34-bd0d-4e99-8cf1-c2a714a504c5)


### Q15) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

### QUERY:
select designation,enumber from manager order by designation ,enumber desc;


### OUTPUT:


![Screenshot 2024-04-02 222116](https://github.com/nandhu6523/DBMS/assets/123856724/4e24da3e-5de7-4b23-b119-012943de5a7e)



## RESULT :
Thus the basic DML commands are executed.
