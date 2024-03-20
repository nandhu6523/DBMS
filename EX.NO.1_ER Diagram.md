# EXP NO 1: ER DIAGRAM CREATION, RELATIONAL MODEL AND SCHEMA GENERATION  
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
![image (2)(1)](https://github.com/DrUmaRaniV/DBMS/assets/123856724/5b668b73-a24f-4362-9d3c-5b50caae6b69)



### Relational model

![image (2)(1)](https://github.com/DrUmaRaniV/DBMS/assets/123856724/1d2f4e35-8011-4d9a-a733-604704a410cf)



### SQL DDL Schema 


last seen today at 11:37 AM
SUNDAY
Seri da
6:37 PM
Mm
6:37 PM
DBMS pathiya
6:38 PM
Ila da enaku Tuesday exam
6:38 PM
Beee
6:38 PM
Adhuku padikanum
6:38 PM
Ok ok
6:38 PM
Pathuakalm ok va
6:38 PM
Mm ma
6:38 PM
Seri da
6:38 PM
You
Pathuakalm ok va
Ok da na Thursday pova da
6:38 PM
Apo
Edited6:38 PM
Dmbs
6:38 PM
Seri da
6:39 PM
Athukulla prepare panilam
6:39 PM
Ok da
6:39 PM
TODAY
image (1).png
PNG•198 kB
11:32 AM
image (2).png
PNG•991 kB
11:32 AM
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
