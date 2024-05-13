# Ex. No: 9  Triggers in PL/SQL
### DATE: 24.04.2024
### REGISTER NUMBER: 212222040050
### AIM: 
To create PL/SQL program to display new and old salary of customer when before/ after updation takes place. 
### PROCEDURE
1. Create a trigger for each row when updation occurs.
2. Declare the variable in Declare section.
3. Start the begin section.
4. Calculate the salary changes.
5. Display the result 
6. End the begin section.
### Program:
```
CREATE OR REPLACE TRIGGER display_salary_changes 
BEFORE DELETE OR INSERT OR UPDATE ON customers 
FOR EACH ROW 
WHEN (NEW.ID > 0) 
DECLARE 
   sal_diff number; 
BEGIN 
   sal_diff := :NEW.salary  - :OLD.salary; 
   dbms_output.put_line('Old salary: ' || :OLD.salary); 
   dbms_output.put_line('New salary: ' || :NEW.salary); 
   dbms_output.put_line('Salary difference: ' || sal_diff); 
END; 
/   
```
### Output:
```
3 row(s) updated.
Old salary: 2500
New salary: 3000
Salary difference: 500
Old salary: 2000
New salary: 2500
Salary difference: 500
```
### Result:
Thust the program was performed sucessfully.
