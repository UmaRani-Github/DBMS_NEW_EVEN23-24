# EX.NO 4 Aggregation functions, Having and Group By clause in SQL
### DATE: 06.03.2024
#### REGISTER NUMBER: 212222040026
## AIM:
To study and write aggregation functions, group by and having clause with suitable examples.
## THEORY
## Aggregation Functions
*An aggregate function is a function that performs a calculation on a set of values, and returns a single value.
*Aggregate functions are often used with the GROUP BY clause of the SELECT statement.
## List of Aggregation functions:
```
1. MIN() - returns the smallest value within the selected column
  Syntax: 
      SELECT MIN(column_name)
      FROM table_name
      WHERE condition;
2. MAX() - returns the largest value within the selected column
  Syntax: 
      SELECT MAX(column_name)
      FROM table_name
      WHERE condition;
3.COUNT() - returns the number of rows in a set
  Syntax: 
      SELECT COUNT(column_name)
      FROM table_name
      WHERE condition; 
4. SUM() - returns the total sum of a numerical column
   Syntax: 
      SELECT SUM(column_name)
      FROM table_name
      WHERE condition;
5.AVG() - returns the average value of a numerical column
	Syntax: 
    SELECT AVG(column_name)
    FROM table_name
    WHERE condition;
```
## GROUP BY CLAUSE
```
GROUP BY: This query is used to group all the records in a relation together for each and every value of a specific key(s) and then display them for a selected set of fields in the relation. 
Syntax: 
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
ORDER BY column_name(s);
```
## HAVING CLAUSE 
```
The HAVING clause was added to SQL because the WHERE keyword could not be used with aggregate functions. The HAVING clause must follow the GROUP BY clause in a query and must also precede the ORDER BY clause if used. 
Syntax: 
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
HAVING condition
ORDER BY column_name(s);
```
## PROCEDURE
```
1. Start the program. 
2. Read the given query.
3. Perform the given aggregation function using MIN(),MAX(),COUNT(),SUM(),AVG().
4. To group all the records in a relation together by GROUP BY clause.
    SELECT column_name(s)
    FROM table_name
    WHERE condition
    GROUP BY column_name(s);
5. To specify the conditions in a grouped records by HAVING clause.
    SELECT column_name(s)
    FROM table_name
    WHERE condition
    GROUP BY column_name(s)
    HAVING condition;
7. Show the output
8. Stop the program
```
### QUERY 
### QUERY 1
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/d6bf153e-3465-401f-8700-e0149e00ae0c)
### SQL QUERY 
SELECT SUM(workhour) AS "Total working hours" FROM employee1;
### TEST QUERY AND ITS OUTPUT  
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/02d61342-fa24-499d-9804-2eba0037faf6)
### QUERY 2
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/a914f5e2-a4cb-495d-ab2d-0d9f9f4ca61d)
### SQL QUERY 
SELECT COUNT(DISTINCT salesman_id) AS COUNT FROM orders;
### TEST QUERY AND ITS OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/a17d11a7-833a-49f1-94e9-39c2ddb0aa7a)
### QUERY 3
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/d9d2cc07-8c4b-4291-987e-c2335fb07034)
### SQL QUERY 
SELECT name, MAX(LENGTH(name)) AS length FROM customer;
### TEST QUERY AND ITS OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/a7b19311-0880-4d02-9915-7142d342172b)
### QUERY 4
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/d3a93337-22e2-4b7d-9146-91bf9467673c)
### SQL QUERY 
```
SELECT 
    CASE
        WHEN (julianday('now') - julianday(DateOfBirth)) / 365.25 < 20 THEN 'Under 20'
        WHEN (julianday('now') - julianday(DateOfBirth)) / 365.25 BETWEEN 20 AND 30 THEN '20-30'
        WHEN (julianday('now') - julianday(DateOfBirth)) / 365.25 BETWEEN 31 AND 40 THEN '31-40'
        WHEN (julianday('now') - julianday(DateOfBirth)) / 365.25 BETWEEN 41 AND 50 THEN '41-50'
        ELSE 'Above 50'
    END AS AgeGroup,
    COUNT(*) AS TotalPatients
FROM Patients
GROUP BY AgeGroup;
```
### TEST QUERY AND ITS OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/c9c6a3e2-84c6-4745-aa2b-86b9efee025b)
### QUERY 5
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/1ffb4344-aa24-4e17-b957-8749cdffdb9e)
### SQL QUERY 
```
SELECT DoctorID, COUNT(*) AS TotalAppointments
FROM Appointments
GROUP BY DoctorID;
```
### TEST QUERY AND ITS OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/1a24b067-deae-48a6-84f0-421f1ed8d356)
### QUERY 6
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/27bac46f-833b-46b6-9bde-a65b21c9db8b)
### SQL QUERY 
SELECT Specialty, Gender, COUNT(*) AS TotalDoctors FROM Doctors GROUP BY Specialty, Gender;
### TEST QUERY AND ITS OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/1a03598a-e3e6-47db-88e6-9f9f35a96570)
### QUERY 7
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/f84c519f-1eca-436b-88e3-9f6fedee9058)
### SQL QUERY
```
SELECT occupation, SUM(workhour)
FROM employee1
GROUP BY occupation
HAVING SUM(workhour) > 20;;
```
### TEST QUERY AND ITS OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/298f87df-f13f-4873-b9dc-8b3a06cd6569)
### QUERY 8
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/3b1c000b-6527-4120-ac51-81e8be1792f4)
### SQL QUERY 
```
SELECT age, AVG(income)
FROM employee
GROUP BY age
HAVING AVG(income) BETWEEN 300000 AND 500000;
```
### TEST QUERY AND ITS OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/d584ad3b-4889-41da-af91-133b81b365f6)
### QUERY 9
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/b61d685e-17d7-41ea-b923-ca63325938d2)
### SQL QUERY 
```
SELECT PatientID, COUNT(*) AS TotalRecords
FROM MedicalRecords
GROUP BY PatientID
HAVING COUNT(*) > 3;
```
### TEST QUERY AND ITS OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/3b7ba8d1-2d4d-42fc-b3ec-6e49a50cfc6f)
### QUERY 10
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/e96fb0e1-b489-4df6-82d1-513e394a0ffb)
### SQL QUERY 
```
SELECT category_id, AVG(Price)
FROM products
GROUP BY category_id
HAVING AVG(Price) BETWEEN 10 AND 15;
```
### TEST QUERY AND ITS OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/9f50599c-dcf0-4ccd-b039-8e8d246dead4)
### RESULT :
Thus the basic aggregation commands are executed.
