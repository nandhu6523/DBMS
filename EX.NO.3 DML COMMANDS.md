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
```
UPDATE manager
SET salary = salary * 1.1;
```
### OUTPUT:
![Screenshot 2024-03-20 113156](https://github.com/22003197/DBMS/assets/124332243/1ef73e78-b0f4-4f91-903c-084a77ac8393)

### Q2) Delete the records from manager table where the salary less than 2750.

### QUERY:
```
DELETE FROM manager
WHERE salary < 2750;
```
### OUTPUT:
![Screenshot 2024-03-20 113351](https://github.com/22003197/DBMS/assets/124332243/9e7975d3-b383-477d-a4ec-db4056bea75f)

### Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)

### QUERY:
```
SELECT ename AS "Name", salary * 12 AS "Annual Salary"
FROM manager;
```
### OUTPUT:
![Screenshot 2024-04-02 134151](https://github.com/22003197/DBMS/assets/124332243/3874fb7b-bb2f-4484-a1d5-7ee3befc1bcd)

### Q5)	List the names of Clerks from emp table.


### QUERY:
```
select ename from manager where designation = 'clerk';
```
### OUTPUT:
![Screenshot 2024-04-02 134226](https://github.com/22003197/DBMS/assets/124332243/a9f96629-5f9e-4948-af5b-889e9201f719)


### Q6)	List the names of employee who are not Managers.


### QUERY:
```
select ename from manager where designation != 'manager';
```
### OUTPUT:
![Screenshot 2024-04-02 134318](https://github.com/22003197/DBMS/assets/124332243/07092244-3b85-4b8b-9132-f32768378238)

### Q7)	List the names of employees not eligible for commission.


### QUERY:
```
select ename from manager where commission = 0;
```
### OUTPUT:

![Screenshot 2024-04-02 134353](https://github.com/22003197/DBMS/assets/124332243/570a9250-c39c-4d33-8d4c-3d9212fc5002)

### Q8)	List employees whose name either start or end with ‘s’.


### QUERY:
```
select ename from manager where ename like 'S%' or ename like '%S';
```
### OUTPUT:
![Screenshot 2024-04-02 134421](https://github.com/22003197/DBMS/assets/124332243/2d80aca9-c5d9-4d58-a22a-af90daa3131b)


### Q9) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.


### QUERY:
```
select Hiredate,ename,designation,deptno from manager order by Hiredate;
```
### OUTPUT:
![Screenshot 2024-04-02 142330](https://github.com/22003197/DBMS/assets/124332243/3a84e254-95fa-407e-a324-e0da09fb2f98)

### Q10) List the Details of Employees who have joined before 30 Sept 81.


### QUERY:
```
select * from manager where hiredate<to_date('1981-09-30','YYYY-MM-DD');
```

### OUTPUT:
![Screenshot 2024-04-02 142422](https://github.com/22003197/DBMS/assets/124332243/446f65d1-14b2-4e63-8fc8-99c0b7ee3a30)


### Q11)	List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.


### QUERY:
```
select ename,deptno,salary from manager order by deptno,salary desc;
```

### OUTPUT:
![Screenshot 2024-04-02 142515](https://github.com/22003197/DBMS/assets/124332243/24bbfa0e-dc86-40f0-a09b-bc76932eafd3)


### Q12) List the names of employees not belonging to dept no 30,40 & 10


### QUERY:
```
select ename from manager where deptno != 30 and deptno != 40 and deptno != 10;
```

### OUTPUT:
![Screenshot 2024-04-02 142553](https://github.com/22003197/DBMS/assets/124332243/8d461fc7-b7de-4286-b5db-44f639466020)

### Q13) Find number of rows in the table EMP

### QUERY:


### OUTPUT:


### Q14) Find maximum, minimum and average salary in EMP table.

### QUERY:


### OUTPUT:


### Q15) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

### QUERY:


### OUTPUT:


## RESULT :
Thus the basic DML commands are executed.
