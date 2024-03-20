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
```
DECLARE
    a NUMBER := 10; 
    b NUMBER := 5;  
    addition_result NUMBER;
    subtraction_result NUMBER;
BEGIN
    addition_result := a + b;
    
    subtraction_result := a - b;
    
    DBMS_OUTPUT.PUT_LINE('Addition Result: ' || addition_result);
    DBMS_OUTPUT.PUT_LINE('Subtraction Result: ' || subtraction_result);
END;
```
### Output:
![Screenshot 2024-03-20 115021](https://github.com/22003197/DBMS/assets/124332243/c57f98ae-26b5-4705-8104-3489b1fdf934)

### Result:
Thust the program was performed sucessfully.
