# EX.NO 4 Aggregation functions, Having and Group By clause in SQL
### DATE:
#### REGISTER NUMBER:
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
### SQL QUERY 
### TEST QUERY AND ITS OUTPUT  
### QUERY 2
### SQL QUERY 
### TEST QUERY AND ITS OUTPUT
### QUERY 3
### SQL QUERY 
### TEST QUERY AND ITS OUTPUT
### QUERY 4
### SQL QUERY 
### TEST QUERY AND ITS OUTPUT
### QUERY 5
### SQL QUERY 
### TEST QUERY AND ITS OUTPUT
### QUERY 6
### SQL QUERY 
### TEST QUERY AND ITS OUTPUT
### QUERY 7
### SQL QUERY 
### TEST QUERY AND ITS OUTPUT
### QUERY 8
### SQL QUERY 
### TEST QUERY AND ITS OUTPUT
### QUERY 9
### SQL QUERY 
### TEST QUERY AND ITS OUTPUT
### QUERY 10
### SQL QUERY 
### TEST QUERY AND ITS OUTPUT
### RESULT :
Thus the basic DML commands are executed.
