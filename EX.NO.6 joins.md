# EX.NO 6 TYPES OF JOINS in SQL
### DATE : 03.04.2024
### REGISTER NUMBER: 212222040050
## AIM:
 To study and implement different types of joins.
# THEORY
## JOINS 
*  The SQL Joins clause is used to combine records from two or more tables in a database.
*  A JOIN is a means for combining fields from two tables by using values common to each.The join is actually performed by the ‘where’ clause which combines specified rows of tables.
## TYPES OF JOINS: 
```
1. Inner Join - The INNER JOIN keyword selects records that have matching values in both tables.
Syntax:
SELECT column_name(s)
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name;
2.Left (Outer) Join -The LEFT JOIN keyword returns all records from the left table (table1), and the matching records from the right table (table2). The result is 0 records from the right side, if there is no match.
Syntax:
SELECT column_name(s)
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;
3.Right (Outer) Join- The RIGHT JOIN keyword returns all records from the right table (table2), and the matching records from the left table (table1). The result is 0 records from the left side, if there is no match.
Syntax:
SELECT column_name(s)
FROM table1
RIGHT JOIN table2
ON table1.column_name = table2.column_name;
4. Full (Outer) Join - The FULL OUTER JOIN keyword returns all records when there is a match in left (table1) or right (table2) table records.
FULL OUTER JOIN and FULL JOIN are the same.
Syntax:
SELECT column_name(s)
FROM table1
FULL OUTER JOIN table2
ON table1.column_name = table2.column_name
WHERE condition;
```
### QUERY 1
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/8670a3a4-4ad4-478e-bc70-a654e7f4e7b9)
### SQL QUERY 
```
SELECT p.admission_date, s.surgery_date
FROM patients p
INNER JOIN surgeries s ON p.patient_id = s.patient_id
```
### OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/b22a3ee9-22db-4d93-897d-5d283f02159b)
### QUERY 2
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/404bb180-95d5-479c-9c06-695085346841)
### SQL QUERY
```
SELECT p.*, d.specialization as doctor_specialization
FROM patients p
INNER JOIN doctors d ON p.doctor_id = d.doctor_id
```
### OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/e6baf2d5-a14a-435f-b5b2-f6ffa9f710b3)
### QUERY 3
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/75d5073d-c6e8-4efb-9a8a-acca9558161b)
### SQL QUERY
```
SELECT n.*, d.department_name
FROM nurses n
INNER JOIN departments d ON n.department_id = d.department_id
```
### OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/9b856963-6912-4aef-a3e9-5251333c6dc0)
### QUERY 4
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/db3f2c2c-5d5b-4087-ab75-f148e942e2e1)
### SQL QUERY
```
SELECT p.first_name,s.*
FROM patients p
INNER JOIN surgeries s ON p.patient_id = s.patient_id
WHERE p.discharge_date BETWEEN '2024-03-01' AND '2024-03-31'
AND p.admission_date NOT BETWEEN '2024-03-01' AND '2024-03-31'
```
### OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/ff40ba94-c751-4893-8113-c2f36671dc5c)
### QUERY 5
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/7cb429d0-981e-4da1-bee0-79b83cc586f0)
### SQL QUERY
```
-- Selecting specific columns from the 'customer' and 'salesman' tables
SELECT a.cust_name, a.city, a.grade, 
       b.name AS "Salesman", b.city 
-- Specifying the tables to retrieve data from ('customer' as 'a' and 'salesman' as 'b')
FROM customer a 
-- Performing a left join based on the salesman_id, including unmatched rows from 'customer'
LEFT JOIN salesman b 
ON a.salesman_id = b.salesman_id 
-- Sorting the result set by customer_id in ascending order
ORDER BY a.customer_id;
```
### OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/273213cf-eb45-43f6-be96-b5e330fa996e)
### QUERY 6
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/0cbce431-9a3e-4748-9abb-183d87466081)
### SQL QUERY
```
SELECT a.cust_name, a.city, a.grade, 
       b.name AS "Salesman", b.city 
-- Specifying the tables to retrieve data from ('customer' as 'a' and 'salesman' as 'b')
FROM customer a 
-- Performing a left outer join based on the salesman_id, including unmatched rows from 'customer'
LEFT OUTER JOIN salesman b 
ON a.salesman_id = b.salesman_id 
-- Filtering the results based on the condition that 'grade' is less than 300
WHERE a.grade < 300 
-- Sorting the result set by customer_id in ascending order
ORDER BY a.customer_id;
```
### OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/a92e8d88-1b19-482c-a6bd-5e587d9bd402)
### QUERY 7
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/79c0c4be-e6de-40da-aeb4-e267a2d84a42)
### SQL QUERY
```
SELECT s.name as salesman_name,  c.cust_name as customer_name
FROM salesman s
LEFT JOIN customer c ON s.salesman_id = c.salesman_id
```
### OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/a79b3dd6-dbc7-47de-95f6-ee088ed92421)
### QUERY 8
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/a66d909d-3d1c-41ed-9b05-ca5743b87fa9)
### SQL QUERY
```
SELECT s.name
FROM salesman s 
LEFT JOIN customer c ON s.salesman_id = c.salesman_id
WHERE c.city = 'London'
```
### OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/5fcc29b4-fd95-4f10-a0cc-4e25f77b781c)
### QUERY 9
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/54ca053b-7da7-4158-9266-ac2395a46318)

### SQL QUERY
```
SELECT c.cust_name , s.name
FROM customer c
LEFT JOIN salesman s on c.salesman_id = s.salesman_id
WHERE c.city == s.city
```
### OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/a5a8cd3b-5fc8-4cef-8d3c-c2a0394b7815)

## QUERY 10
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/5fcd3eaa-5929-4c07-a85b-38baa215d9d5)
### SQL QUERY
```
SELECT s.*
FROM customer c
LEFT JOIN salesman s on c.salesman_id = s.salesman_id
WHERE c.cust_name = 'Fabian Johns'
```
### OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/ffb00fe6-5021-46ee-afe1-0076e0894818)
## RESULT :
Thus the different type of JOINS are executed.
