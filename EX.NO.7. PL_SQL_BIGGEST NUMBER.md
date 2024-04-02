# Ex. No: 6 PL/SQL program -BIGGEST OF THREE NUMBERS  
### DATE: 
### AIM: To create PL/SQL program to find biggest of three numbers.

### ALGORITHM:
1. Declare the variable a, b, c and assign value in Declare section.
2. begin the section
3. Find biggest of three numbers 
4. 5. Display the result 
6. End the begin section.

### Program:
'''
 DECLARE
       a NUMBER := 10; 
       
       b NUMBER := 20; 
       
       c NUMBER := 15; 
       
       biggest NUMBER;
 BEGIN
      IF a >= b AND a >= c THEN
      
         biggest := a;
         
     ELSIF b >= a AND b >= c THEN
     
         biggest := b;
         
     ELSE
     
         biggest := c;
         
     END IF;
    
    DBMS_OUTPUT.PUT_LINE('The biggest of ' || a || ', ' || b || ', and ' || c || ' is: ' || biggest);
END;


### Output:
![Screenshot 2024-04-02 215657](https://github.com/nandhu6523/DBMS/assets/123856724/0827623e-5725-4068-b080-8944cc8644fb)




### Result:
Thust the program was performed sucessfully.
