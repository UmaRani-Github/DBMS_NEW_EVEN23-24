# EXP NO 2: DATA DEFINITION LANGUAGE COMMANDS AND ITS CONSTRAINTS
### DATE : 21.02.2024
### REGISTER NUMBER: 212222240054
## AIM:
 To study and write DDL commands and different types of constraints.
## THEORY
```
### DDL (Data Definition Language)
* DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema.
* It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.
* DDL is a set of SQL commands used to create, modify, and delete database structures but not data.
* These commands are normally not used by a general user, who should be accessing the database via an application.
### List of DDL commands: 
1. CREATE: This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).
   Syntax:CREATE TABLE (field_1 data_type(size),field_2 data_type(size), .. . );
2. ALTER: This is used to alter the structure of the database.
   A) To add new column
   Syntax: ALTER TABLE relation_name ADD (new field_1 data_type(size) );
   B) To modify the data type of existing column
   Syntax: ALTER TABLE relation_name MODIFY (field_1 newdata_type(Size)
   C) To drop the column of table
    Syntax:ALTER TABLE relation_name DROP COLUMN (field_name); 
   D) To rename the column of table
   Syntax: ALTER TABLE relation_name RENAME COLUMN (OLD field_name) to (NEW field_name);
3. DROP TABLE :This is used to delete the structure of a relation. It permanently deletes the records in the table.
   Syntax: DROP TABLE relation_name;
4. RENAME: This is used to rename an object existing in the database.
   Syntax: RENAME TABLE old_relation_name TO new_relation_name;     
### CONSTRAINTS
Constraints are used to specify rules for the data in a table. If there is any violation between the constraint and the data action, the action is aborted by the constraint. It can be specified when the table is created (using CREATE TABLE statement) or after the table is created (using ALTER TABLE statement). 
1. NOT NULL:
   When a column is defined as NOTNULL, then that column becomes a mandatory column. It implies that a value must be entered into the column if the record is to be accepted for storage in the table. 
Syntax:
 CREATE TABLE Table_Name (column_name data_type (size) NOT NULL, );
2. UNIQUE: The purpose of a unique key is to ensure that information in the column(s) is unique i.e. a value entered in column(s) defined in the unique constraint must not be repeated across the column(s). A table may have many unique keys. 
Syntax:
CREATE TABLE Table_Name(column_name data_type(size) UNIQUE, ….);
3. CHECK: Specifies a condition that each row in the table must satisfy. To satisfy the constraint, each row in the table must make the condition either TRUE or unknown (due to a null). 
Syntax:
CREATE TABLE Table_Name(column_name data_type(size) CHECK(logical expression), ….); 
4. PRIMARY KEY: A field which is used to identify a record uniquely. A column or combination of columns can be created as primary key, which can be used as a reference from other tables. A table contains primary key is known as Master Table.  
*It must uniquely identify each record in a table.  
*It must contain unique values.  
*It cannot be a null field. 
*It cannot be a multi port field.  
*It should contain a minimum number of fields necessary to be called unique. 
Syntax:
CREATE TABLE Table_Name(column_name data_type(size) PRIMARY KEY, ….);
5. FOREIGN KEY: It is a table level constraint. We cannot add this at column level. To reference any primary key column from other table this constraint can be used. The table in which the foreign key is defined is called a detail table. The table that defines the primary key and is referenced by the foreign key is called the master table. 
Syntax:
CREATE TABLE Table_Name(column_name data_type(size) FOREIGN KEY(column_name) REFERENCES table_name);
6. DEFAULT : The DEFAULT constraint is used to insert a default value into a column. The default value will be added to all new records, if no other value is specified. 
Syntax:
CREATE TABLE Table_Name(col_name1,col_name2,col_name3 DEFAULT ‘’);
```
## PROCEDURE
1. Start the program. 
2. Read the given query.
3. create the table using 
        CREATE TABLE (field_1 data_type(size),field_2 data_type(size), .. . );
4. Drop the table by  DROP TABLE relation_name;
5. Alter the table structure of the database by ALTER TABLE relation_name ADD (new field_1 data_type(size) );
6. Specify the constraints NOT NULL,UNIQUE,DEFAULT,UNIQUE based on the query
7. Show the output
8. Stop the program
## Query 1:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/908acbce-7e1f-49ca-b8b5-9dca4e8aef38)
### SQL QUERY:
CREATE TABLE Employee (eid INTEGER PRIMARY KEY AUTOINCREMENT,name VARCHAR(50),designation VARCHAR(30));
### OUTPUT TEST CASE:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/c0f06a33-4afd-4c30-b74b-8ffb47f022a6)
### Query 2:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/9ffc13e7-7791-46e5-b648-2aa451948bec)
### SQL QUERY: 
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/fdbfa19a-cd78-44b2-ac75-dd9e0c1382c9)
### OUTPUT TEST CASE:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/3135af0b-9d2f-4049-a778-3b461e12d7b5)
### Query 3:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/64cb1b20-455b-4852-816f-d11c48a153ab)
### SQL QUERY: 
```
INSERT INTO CUSTOMERS (ID,NAME,AGE,ADDRESS,SALARY)
VALUES (1, 'Ramesh', 32, 'Ahmedabad', 2000.00 );
INSERT INTO CUSTOMERS (ID,NAME,AGE,ADDRESS,SALARY)
VALUES (2, 'Khilan', 25, 'Delhi', 1500.00 );
INSERT INTO CUSTOMERS (ID,NAME,AGE,ADDRESS,SALARY)
VALUES (3, 'Kaushik', 23, 'Kota', 2000.00 );
```
### OUTPUT TEST CASE:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/220387c6-f6e8-4aef-8617-24ec6e677c3e)

### Query 4:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/080001f3-6034-4271-a376-19f72cf0df5a)

### SQL QUERY: 
```
INSERT INTO Student (RollNo, Name, Gender, Subject, MARKS) VALUES 
 (3, 'Jeni', 'Female', 'English', 96),
  (4, 'Bob Johnson', 'Male', 'History', 90),
   (5, 'Sharvesh', 'Male', 'Botany', 97),
     (6, 'Mathew', 'Male', 'Science', 85);
```
### OUTPUT TEST CASE:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/3471a64b-65b5-43b5-8862-f8e4072e0674)
### Query 5:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/1103ce7b-37c3-4243-a351-8d1206cb7476)
### SQL QUERY: 
```
INSERT INTO DestinationTable (ID, Name, Age)
SELECT ID, Name, Age
FROM SourceTable
WHERE Age<25;
```
### OUTPUT:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/ac597de4-334d-4391-920e-8374e35be76f)
### Query 6:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/eb2ec792-5e04-4107-b5f7-4e66d490fe0d)
### SQL QUERY: 
ALTER TABLE employee ADD designation varchar(50);
### OUTPUT:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/68559357-138b-46fc-a753-91458e93e0e6)
### Query 7:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/62b82b22-02eb-418e-9763-a887d3f297d8)
### SQL QUERY: 
ALTER TABLE Student_details ADD Country TEXT;
### OUTPUT:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/0ae97674-b109-4970-a9f8-ffff9b9ba43e)
### Query 8:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/414793c7-c72e-434a-b6e4-9029a28de61a)
### SQL QUERY: 
ALTER TABLE Student_details ADD Date_of_birth Date;
### OUTPUT:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/036569e4-0874-4143-8240-958883674ee8)
### Query 9:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/062c6676-73e8-4350-87d3-e34af019aa7e)
### SQL QUERY: 
```
CREATE TABLE Employee (
eid integer NOT NULL,
name varchar(50),
mobilenumber number,UNIQUE(eid));
```
### OUTPUT:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/f609fc64-365e-4f86-a68e-e52693110911)
### Query 10:

### SQL QUERY: 
```
CREATE TABLE Orders (
    OrderID INTEGER ,
    OrderNumber INTEGER,
    ProductName Varchar(30),
    PersonID INTEGER not null,
    FOREIGN KEY (PersonID) REFERENCES Person(PersonID)
    Unique(OrderID)
);
```
### OUTPUT:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/19255c37-d71d-498e-a3a7-d5974e2de08c)

## Result:
         Thus the basic DDL commands and constraints in SQL are executed. 


