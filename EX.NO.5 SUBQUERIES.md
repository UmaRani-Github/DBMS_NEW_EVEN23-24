# EX.NO 5 Sub Queries and Views in SQL
### DATE:20.03.2024
#### REGISTER NUMBER:212222040036
## AIM:
To study and implement Subqueries and Views in SQL 
## THEORY
## SUB QUERIES 
* The query within another is known as a subquery. A statement containing a subquery is called a parent statement.
* A subquery may occur in :
- A SELECT clause
- A FROM clause
- A WHERE clause
*The subquery can be nested inside a SELECT, INSERT, UPDATE, or DELETE statement or inside another subquery.
## Types of SubQueries
1. Sub queries that return several values - Sub queries can also return more than one value. Such results should be made use along with the operators in and any.
2. Multiple queries- Here more than one subquery is used. These multiple sub queries are combined by means of ‘and’ & ‘or’ keywords. 
3. Correlated subquery- A subquery is evaluated once for the entire parent statement whereas a correlated Sub query is evaluated once per row processed by the parent statement.
## Views
```
In SQL, a view is a virtual table based on the result-set of an SQL statement. A view contains rows and columns, just like a real table. The fields in a view are fields from one or more real tables in the database. 
Syntax: 
CREATE VIEW 
AS 
SELECT FROM relation_name WHERE (Condition);
To drop a view by
Syntax: DROP VIEW viewname;
```
## PROCEDURE
```
1. Start the program. 
2. Read the given query.
3. Write the sub query for a given query.
4. Create a view using
	CREATE VIEW 
	AS 
	SELECT FROM relation_name WHERE (Condition);
5. Show the output
6. Stop the program
```
### QUERY 
### QUERY 1
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/aa352852-f1d3-4c43-bb4e-7aabdec31262)
### SQL QUERY 
```
SELECT *
FROM orders
WHERE purch_amt >
    (SELECT avg(purch_amt)
     FROM orders 
     WHERE ord_date = '2012-10-10');
```
### TEST QUERY AND ITS OUTPUT 
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/8212ebd5-7e8a-41ec-8edc-c1d6ad39d11c)
### QUERY 2
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/fc3072fe-3330-4c95-b3c8-cc2bf55f6286)
### SQL QUERY 
```
SELECT *
FROM customer
WHERE customer_id =
    (SELECT salesman_id - 2001
     FROM salesman
     WHERE name = 'Mc Lyon');
     ```
### TEST QUERY AND ITS OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/c7dae58e-3c29-4bf5-88cb-40b86b2cd4f9)
### QUERY 3
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/9c22fa7e-be93-4e36-a376-545a0a95076b)
### SQL QUERY
```
SELECT *
FROM grades t1
WHERE grade = (
    SELECT Min(grade)
    FROM grades t2
    WHERE t2.subject = t1.subject
);
```
### TEST QUERY AND ITS OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/8a84bbcd-d2e6-417a-8ee3-f0351679dd63)
### QUERY 4
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/862a4cd5-a8b3-4405-9794-4c4a09301ad4)
### SQL QUERY
```
SELECT *
FROM orders
WHERE salesman_id IN
    (SELECT salesman_id 
     FROM salesman 
     WHERE city='New York');
```
### OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/0c9b5fb9-d875-4358-babe-0c725e8473e2)
### QUERY 5
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/90f255d2-12b1-4cae-a033-dd9474b4589b)
### SQL QUERY
SELECT * FROM CUSTOMERS WHERE ID IN (SELECT ID FROM CUSTOMERS WHERE Address="Delhi" and age <30);
###  OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/51e8e128-5a27-46bb-9a31-7d7ba2fe92e8)
### QUERY 6
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/4d4e8238-6f6f-42e6-beae-2520a6691e48)
### SQL QUERY
```
SELECT *
FROM employee
WHERE age < (SELECT AVG(age) FROM employee WHERE income > 250000);
```
### OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/bcfe7434-8ca2-4ee7-8fe4-743567a1c842)
### QUERY 7
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/77874943-ee10-4e4b-8ccd-452ed8488f98)
### SQL QUERY
SELECT * FROM CUSTOMERS WHERE ID IN (SELECT ID FROM CUSTOMERS WHERE SALARY > 1500);
### OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/69fa4e7e-b59f-46d4-b68d-8eb26d3a31aa)
### QUERY 8
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/b7117032-3373-41e0-bd05-ddb6755e0ad6)
### SQL QUERY
```
SELECT name, city
FROM customer
WHERE city IN (SELECT city FROM customer WHERE id IN (3, 7));
```
### OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/20bcb000-5e23-40ff-a6f0-44d37359cfd2)
### QUERY 9
Create a table
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/749f06bf-dbbb-403e-8291-5cc32a256861)
after insertion of three rows, Create a view v1 which contain name and address column only.
### SQL QUERY
```
CREATE VIEW v1 AS
SELECT NAME, ADDRESS
FROM StudentDetails1
WHERE S_ID < 5;
```
### TEST QUERY AND ITS OUTPUT
SELECT * FROM v1;
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/ed008658-1152-4e5f-962e-b97b66cd062c)
### QUERY 10
Delete a view v1.
### SQL QUERY
drop view v1;
### TEST QUERY AND ITS OUTPUT
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/c9803a3f-0708-438b-a958-f626d748339e)
SELECT * FROM v1;
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/fcc076ad-b913-4773-a458-adcb7fc51d19)
### RESULT :
Thus the sub queries and views are executed.
