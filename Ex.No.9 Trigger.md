# Ex. No: 6 PL/SQL program using Triggers 
### DATE: 
### AIM: To create PL/SQL program to display new and old salary of customer when before/ after updation takes place. 

### Steps:
1. Create a trigger for each row when updation occurs.
2. Declare the variable in Declare section.
3. Start the begin section.
4. Calculate the salary changes.
5. Display the result 
6. End the begin section.

### Program:
```
create table customers(ID int,NAME varchar(20),AGE int,ADDRESS varchar(20),salary int);
insert into customers values( 1,'Ramesh',32,'Ahmedabad',2000);
insert into customers values( 1,'Khilan',25,'Delhi',1500);
insert into customers values( 1,'kaushik ',23,'Kota',2000);
DECLARE 
   c_id customers.id%type; 
   c_name customers.name%type; 
   c_addr customers.address%type; 
   CURSOR c_customers is 
      SELECT id, name, address FROM customers; 
BEGIN 
   OPEN c_customers; 
   LOOP 
   FETCH c_customers into c_id, c_name, c_addr; 
      EXIT WHEN c_customers%notfound; 
      dbms_output.put_line(c_id || ' ' || c_name || ' ' || c_addr); 
   END LOOP; 
   CLOSE c_customers; 
END; 
/
```
### Output:
![Screenshot 2024-04-03 105623](https://github.com/nandhu6523/DBMS/assets/123856724/e7e45d91-21c4-4094-9860-84b33297b632)

### Result:
Thust the program was performed sucessfully.
