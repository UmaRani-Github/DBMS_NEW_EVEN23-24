# EX.NO 3 Data Manipulation Language (DML) Commands and built in functions in SQL
### DATE: 28.02.2024
#### REGISTER NUMBER: 212222040050
## AIM:
To Study and write DML Commands for given query.
## THEORY
## DML(Data Manipulation Language)
*  The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements.
*  It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.
## List of DML commands:
```
1. INSERT: It is used to insert data into a table
Types of INSERT COMMAND
a) Inserting a single record 
  Syntax:
   INSERT INTO < relation/table name> (field_1,field_2……field_n)VALUES (data_1,data_2, ...... data_n);
b) Inserting all records from another relation
  Syntax:
   INSERT INTO relation_name_1 SELECT Field_1,field_2,field_n FROM relation_name_2 WHERE field_x=data;
c) Inserting multiple records 
  Syntax:
    INSERT INTO relation_name field_1,field_2, ....field_n) VALUES (&data_1,&data_2,.......&data_n); 
2. UPDATE: It is used to update existing data within a table.
   Syntax:
   UPDATE relation name SET Field_name1=data,field_name2=data, WHERE field_name=data;
3. DELETE: It is used to delete records from a database table.
   a) DELETE-FROM: This is used to delete all the records of relation. 
   Syntax
   DELETE FROM relation_name;
   b) DELETE -FROM-WHERE: This is used to delete a selected record from a relation. 
   Syntax: DELETE FROM relation_name WHERE condition;
4. SELECT: The SELECT command shows the records of the specified table.
   Syntax: 
   SELECT (column1,column2) FROM (Table Name)WHERE condition;
```
## PROCEDURE
```
1. Start the program. 
2. Read the given query.
3. insert values into the table using 
   INSERT INTO < relation/table name> (field_1,field_2……field_n)VALUES (data_1,data_2, ...... data_n);
4. Update the existing data within a table by UPDATE command by
   UPDATE relation name SET Field_name1=data,field_name2=data, WHERE field_name=data;
5. Delete the records in a table by DELETE command
   DELETE FROM relation_name WHERE condition;
6. Use  SELECT command shows the records of the specified table.
     SELECT (column1,column2) FROM (Table Name)WHERE condition;
7. Show the output
8. Stop the program
```
## QUERY 
## QUERY 1
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/14403ec0-4bdf-4f4d-9493-c1e89a3eb969)
## SQL QUERY 
select categoryName,description from categories order by categoryName;
## TEST QUERY AND ITS OUTPUT  
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/e876a627-d587-4dc1-a47b-5bdbf6a6f3dd)
## QUERY 2
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/1ecc7406-81b9-49a8-87af-1060e3259731)
## SQL QUERY 
SELECT * FROM customer WHERE city = 'London' AND grade > 200;
## TEST QUERY AND ITS OUTPUT  
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/0f5944aa-17e2-480d-89ad-3cae7e530a42)
## QUERY 3
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/c868fa42-61b9-465f-85a7-34ab2c23d23f)
## SQL QUERY
SELECT * FROM orders WHERE (purch_amt < 200 OR NOT (ord_date >= '2012-02-10' AND customer_id < 3009));
## TEST QUERY AND ITS OUTPUT 
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/f5af2a79-6e77-4687-9fb9-e94caf16f945)
# QUERY 4
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/334b9113-b1e1-4762-a92e-72bbd778938c)
## SQL QUERY 
SELECT * FROM customer WHERE grade IS NULL;
## TEST QUERY AND ITS OUTPUT  
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/3d1e613c-c356-4806-85ef-32f35f2949ee)
## QUERY 5
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/683b7c1b-d5f6-43bd-a8ea-17116b586615)
## SQL QUERY 
DELETE FROM surgeries WHERE  surgery_id = 3 or  surgeon_id = 4;
## TEST QUERY AND ITS OUTPUT 
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/42b96061-dd53-4921-975f-99ee9f9c176d)
## QUERY 6
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/ec654473-157e-4113-842b-954c6ad04675)
## SQL QUERY 
DELETE FROM customer WHERE OPENING_AMT BETWEEN 4000 AND 6000;
## TEST QUERY AND ITS OUTPUT 
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/c037a869-d401-4765-b88d-87e5e40287c4)
## QUERY 7
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/a3493209-8ced-4051-b2f7-4a7c9c399790)
## SQL QUERY 
DELETE FROM customer WHERE LENGTH(CUST_NAME) = 6;
## TEST QUERY AND ITS OUTPUT 
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/317e2d2d-55bd-4b6a-86ad-fa188f0c219c)
## QUERY 8
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/4900a11a-967d-4e3b-b77c-c63f807136c9)
## SQL QUERY
UPDATE products SET product_name = 'Grapefruit' WHERE product_id = 4;
## TEST QUERY AND ITS OUTPUT 
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/221f80e8-fbbd-4f49-8b33-c26e921f5d14)
## QUERY 9
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/d3ef85de-b0f9-4e7a-9149-0f9606028daa)
## SQL QUERY 
UPDATE suppliers SET supplier_name = 'A1 Suppliers' WHERE supplier_id = 8;
## TEST QUERY AND ITS OUTPUT 
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/c6ebd25e-606f-4db9-8dde-d38bb7a50508)
## QUERY 10
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/cab90fce-a721-4318-8424-54f4f2258e9c)
## SQL QUERY 
UPDATE products SET reorder_lvl = 40  WHERE category = 'Grocery';
## TEST QUERY AND ITS OUTPUT 
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/a2da7c2d-4321-45e0-a1ea-20fabd42e805)


## RESULT :
Thus the basic DML commands are executed.
