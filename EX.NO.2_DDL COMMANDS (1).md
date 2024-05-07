# EXP NO 2: DATA DEFINITION LANGUGE COMMANDS AND ITS CONSTRAINTS
### DATE
## AIM:
 To study and implement DDL commands and different types of constraints.

## THEORY
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
## PROCEUDRE
STEP 1. Start the program. 
STEP 2 : Read the given query.
STEP 3: create the table using 
        CREATE TABLE (field_1 data_type(size),field_2 data_type(size), .. . );
STEP 4: 

## Query:
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/908acbce-7e1f-49ca-b8b5-9dca4e8aef38)
### SQL QUERY:
CREATE TABLE Employee (eid INTEGER PRIMARY KEY AUTOINCREMENT,name VARCHAR(50),designation VARCHAR(30));
### OUTPUT:
pragma table_info('Employee');
cid    name   typ  notnull     dflt_value  pk
-----  -----  ---  ----------  ----------  ----------
0      eid    INT  0                       1
1      name   VAR  0                       0
2      desig  VAR  0                       0

### 2) Create a table name as "Students" with the following attributes
ATTRIBUTE	id	name	address	grades	phone
DATATYPE	INTEGER PRIMARY KEY AUTOINCREMENT	VARCHAR(50)	VARCHAR(30)	varchar(10)	number
id as integer primarykey with autoincrement
name as varchar(50)
address as varchar(30)
grades as varchar(10)
phone as number

### SQL QUERY: 


### OUTPUT:

### 3) Alter the above student table by adding another attribute department

### SQL QUERY: 

### OUTPUT:

### 4) Rename the student table to mystudent

### SQL QUERY: 



### OUTPUT:

### 5) Delete the mystudent rows using truncate keyword

### SQL QUERY: 


### OUTPUT:
### 4) Drop the mystudent table
 
### SQL QUERY: 


### OUTPUT:








## Result:
         Thus the basic DDL commands in SQL are executed. 


