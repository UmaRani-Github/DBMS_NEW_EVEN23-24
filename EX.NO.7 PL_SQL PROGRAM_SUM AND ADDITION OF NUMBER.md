# Ex.No: 7 PL/SQL program to perform addition and subtraction of two number 
### DATE: 10.04.2024
### REGISTER NUMBER: 212222040050
### AIM: To create PL/SQL program to perform addition and subtraction of two number.
### PROCEDURE
1. Declare the variable a, b and necessary variables in Declare section.
2. Perform addition of two numbers
3. Perform subtraction of two numbers 
4. Display the result 
5. End the begin section.
### Program:
```
declare
-- declare variable x, y 
-- and z of datatype number
x number(5);             
y number(5);            
S number(7); 
A number(7); 
begin
-- Here we Assigning 10 into x
x:=10;                 
-- Assigning 20 into x
y:=20;                 
-- Assigning sum of x and y into z
A:=x+y;                 
S:=x-y;
-- Print the Result
dbms_output.put_line('Addition is '||A); 
dbms_output.put_line('subtraction is '||S); 
end; 
/                       
```
### Output:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/84a57942-2877-4d2d-9a80-42b0c6ba8916)
### Result:
Thust the program was performed sucessfully.
