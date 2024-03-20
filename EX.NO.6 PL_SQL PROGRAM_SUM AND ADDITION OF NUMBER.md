# Ex. No: 6 PL/SQL program to perform addition and subtraction of two number 
### DATE: 
### AIM: To create PL/SQL program to perform addition and subtraction of two number.

### Steps:
1. Declare the variable a, b and necessary variables in Declare section.
2. Perform addition of two numbers
3. Perform subtraction of two numbers 
4. Display the result 
5. End the begin section.

### Program:
SET SERVEROUTPUT ON;

DECLARE
    num1 NUMBER := 10;
    
    num2 NUMBER := 5;
    
    result_add NUMBER;
    
    result_sub NUMBER;
    
BEGIN
    -- Addition
    
    result_add := num1 + num2;
    
    DBMS_OUTPUT.PUT_LINE('Addition Result: ' || result_add);

    -- Subtraction
    
    result_sub := num1 - num2;
    
    DBMS_OUTPUT.PUT_LINE('Subtraction Result: ' || result_sub);
END;


### Output:
![Screenshot 2024-03-20 115522](https://github.com/nandhu6523/DBMS/assets/123856724/215c95de-02be-4ae8-b712-12d1d0bb154c)



### Result:
Thust the program was performed sucessfully.
