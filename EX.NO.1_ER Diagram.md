# EX.NO 1: ER DIAGRAM CREATION, RELATIONAL MODEL AND SCHEMA GENERATION  
### DATE:14.02.2024 
### REGISTER NUMBER: 212222040050
## AIM:
<div align="justify">
   To create an ER Diagram for University Data base or Hospital data base using ERD Plus tool and generate the relational model with schema. 
</div>
## Algorithm
1. Create a login with https://erdplus.com.
2. Create a new ER Diagram with name
3. Create a strong entity, relation and attributes.
4. Create a weak entity, relation and attributes.
5. Specify attributes unique, multivalued and composite attributes.

### ER Diagram 
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/3d55670f-6398-418e-af51-6b654c007b93)


### Relational model
![image](https://github.com/UmaRani-Github/DBMS_NEW_EVEN23-24/assets/144427076/96d8d7cb-01e2-4129-b640-03f3085eca53)

### SQL DDL Schema 
'''CREATE TABLE Programs
(
  pro_id INT NOT NULL,
  pro_name INT NOT NULL,
  pro_dept INT NOT NULL,
  PRIMARY KEY (pro_id)
);

CREATE TABLE Courses
(
  course_no INT NOT NULL,
  co_name INT NOT NULL,
  credits INT NOT NULL,
  PRIMARY KEY (course_no)
);

CREATE TABLE Instructors
(
  staff_no INT NOT NULL,
  staff_name INT NOT NULL,
  PRIMARY KEY (staff_no)
);

CREATE TABLE Students
(
  adm_n0 INT NOT NULL,
  stu_name INT NOT NULL,
  age INT NOT NULL,
  phone INT NOT NULL,
  email INT NOT NULL,
  PRIMARY KEY (adm_n0)
);

CREATE TABLE slots
(
  sem INT NOT NULL,
  year INT NOT NULL,
  room_no INT NOT NULL,
  Date_and_Time INT NOT NULL,
  adm_n0 INT NOT NULL,
  PRIMARY KEY (Date_and_Time),
  FOREIGN KEY (adm_n0) REFERENCES Students(adm_n0)
);

CREATE TABLE Teaches
(
  Date_and_Time INT NOT NULL,
  staff_no INT NOT NULL,
  PRIMARY KEY (Date_and_Time, staff_no),
  FOREIGN KEY (Date_and_Time) REFERENCES slots(Date_and_Time),
  FOREIGN KEY (staff_no) REFERENCES Instructors(staff_no)
);

CREATE TABLE prerequisites
(
  pro_id INT NOT NULL,
  course_no INT NOT NULL,
  PRIMARY KEY (pro_id, course_no),
  FOREIGN KEY (pro_id) REFERENCES Programs(pro_id),
  FOREIGN KEY (course_no) REFERENCES Courses(course_no)
);

CREATE TABLE convenient
(
  course_no INT NOT NULL,
  Date_and_Time INT NOT NULL,
  PRIMARY KEY (course_no, Date_and_Time),
  FOREIGN KEY (course_no) REFERENCES Courses(course_no),
  FOREIGN KEY (Date_and_Time) REFERENCES slots(Date_and_Time)
);

CREATE TABLE Instructors_contact_no
(
  contact_no INT NOT NULL,
  staff_no INT NOT NULL,
  PRIMARY KEY (contact_no, staff_no),
  FOREIGN KEY (staff_no) REFERENCES Instructors(staff_no)
);

CREATE TABLE Departments
(
  Dname INT NOT NULL,
  HOD INT NOT NULL,
  Dphone INT NOT NULL,
  staff_no INT NOT NULL,
  adm_n0 INT NOT NULL,
  PRIMARY KEY (Dname),
  FOREIGN KEY (staff_no) REFERENCES Instructors(staff_no),
  FOREIGN KEY (adm_n0) REFERENCES Students(adm_n0)
);

CREATE TABLE Offers
(
  Dname INT NOT NULL,
  pro_id INT NOT NULL,
  PRIMARY KEY (Dname, pro_id),
  FOREIGN KEY (Dname) REFERENCES Departments(Dname),
  FOREIGN KEY (pro_id) REFERENCES Programs(pro_id)
);

CREATE TABLE College
(
  Cname INT NOT NULL,
  Cphone INT NOT NULL,
  Coffice INT NOT NULL,
  Dname INT NOT NULL,
  staff_no INT NOT NULL,
  PRIMARY KEY (Cname),
  FOREIGN KEY (Dname) REFERENCES Departments(Dname),
  FOREIGN KEY (staff_no) REFERENCES Instructors(staff_no)
); '''
## RESULT 
<div align="justify">
Thus the ER diagram was drawn and relational diagram, SQL DDL staements are generated using ERD plus tool.
</div>
