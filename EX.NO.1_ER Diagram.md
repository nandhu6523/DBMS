![image (2)(1)](https://github.com/nandhu6523/DBMS/assets/123856724/795f3449-a755-45a1-8aaf-93225943dba5)# EXP NO 1: ER DIAGRAM CREATION, RELATIONAL MODEL AND SCHEMA GENERATION  
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
![image (2)(1)](https://github.com/nandhu6523/DBMS/assets/123856724/7438194d-ea47-4645-b275-ed87dce8e887)





### Relational model
![image (1)](https://github.com/nandhu6523/DBMS/assets/123856724/8a566e9a-695d-4740-9be9-50e9dc39cc2d)



### SQL DDL Schema 
'''
   CREATE TABLE Instructor
  (
    I_id INT NOT NULL,
    
    Full_name INT NOT NULL,
    
    Email INT NOT NULL,
    
    PRIMARY KEY (I_id)
 );

 CREATE TABLE Department
 (
   D_id INT NOT NULL,
   D_name INT NOT NULL,
   PRIMARY KEY (D_id)
 );

CREATE TABLE Instructor_phone.no
(
  phone.no INT NOT NULL,
  I_id INT NOT NULL,
  PRIMARY KEY (phone.no, I_id),
  FOREIGN KEY (I_id) REFERENCES Instructor(I_id)
);

CREATE TABLE Student
(
  S_id INT NOT NULL,
  Fname INT NOT NULL,
  Lnmae INT NOT NULL,
  DOB INT NOT NULL,
  Email INT NOT NULL,
  D_id INT NOT NULL,
  PRIMARY KEY (S_id),
  FOREIGN KEY (D_id) REFERENCES Department(D_id)
);

CREATE TABLE Program
(
  P_id INT NOT NULL,
  P_Name INT NOT NULL,
  D_id INT NOT NULL,
  PRIMARY KEY (P_id),
  FOREIGN KEY (D_id) REFERENCES Department(D_id)
);

CREATE TABLE Course
(
  C_number INT NOT NULL,
  C_name INT NOT NULL,
  Credits INT NOT NULL,
  D_id INT NOT NULL,
  PRIMARY KEY (C_number),
  FOREIGN KEY (D_id) REFERENCES Department(D_id)
);

CREATE TABLE Enrollment
(
  E_id INT NOT NULL,
  E_date INT NOT NULL,
  S_id INT NOT NULL,
  C_number INT NOT NULL,
  PRIMARY KEY (E_id),
  FOREIGN KEY (S_id) REFERENCES Student(S_id),
  FOREIGN KEY (C_number) REFERENCES Course(C_number),
  UNIQUE (S_id, C_number)
);

CREATE TABLE Teaches
(
  C_number INT NOT NULL,
  I_id INT NOT NULL,
  PRIMARY KEY (C_number, I_id),
  FOREIGN KEY (C_number) REFERENCES Course(C_number),
  FOREIGN KEY (I_id) REFERENCES Instructor(I_id)
);

CREATE TABLE Student_phone.no
(
  phone.no INT NOT NULL,
  S_id INT NOT NULL,
  PRIMARY KEY (phone.no, S_id),
  FOREIGN KEY (S_id) REFERENCES Student(S_id)
);


## RESULT 
<div align="justify">
Thus the ER diagram was drawn and relational diagram, SQL DDL staements are generated using ERD plus tool.
</div>
