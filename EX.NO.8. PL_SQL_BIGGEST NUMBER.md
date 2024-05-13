# Ex.No:8 PL/SQL program -BIGGEST OF THREE NUMBERS  
### DATE: 17.04.2024
### REGISTER NUMBER: 212222040050
### AIM: 
To create PL/SQL program to find biggest of three numbers.
### ALGORITHM:
1. Declare the variable a, b, c and assign value in Declare section.
2. begin the section
3. Find biggest of three numbers 
4. Display the result 
6. End the begin section.
### Program:
```
--To find the greatest number among given three numbers
DECLARE
    --a assigning with 46 
    a NUMBER := 46; 
    --b assigning with 67 
    b NUMBER := 67; 
    --c assigning with 21 
    c NUMBER := 21; 
BEGIN
    --block start 
    --If condition start 
    IF a > b 
       AND a > c THEN
      --if a is greater then print a 
      dbms_output.Put_line('Greatest number is '
                           ||a); 
    ELSIF b > a 
          AND b > c THEN
      --if b is greater then print b 
      dbms_output.Put_line('Greatest number is '
                           ||b); 
    ELSE
      --if c is greater then print c 
      dbms_output.Put_line('Greatest number is '
                           ||c); 
    END IF; 
--end if condition 
END; 
--End program
```
### Output:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/43870e84-6346-483e-8f5e-431db674a7dd)
### Result:
Thust the PL/SQL program was performed sucessfully.
