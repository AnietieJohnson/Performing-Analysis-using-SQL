# STUDENT RECORD DATABASE PROJECT
## Introduction
This project aims to showcase the creation and management of a database designed to store essential information about students. The database will consist of three main tables: Students Info, Health Records, and Performance. This project requires setting up a database, creating tables, defining constraints, and making modifications as required.
## Project Objective 1
1. Create a Database named “Students Record”
2. Create the following tables in the database create:
   - Students Info  (Student ID, Gender, Name, Age, Subject)
   - Health records (Student ID, Blood Group, Height, Weight)
   - Performance (Student ID, Score, Grade)
3. The ID has to be unique
4. Where a student has no score, it should be ‘0’ by default
5. Add a constraint that prevents the ID and Subject from taking null values
6. Apply the following modifications to the table
   - Change column name ‘’Subject” to ‘’Course” 
   - Drop the “Age” column from the ‘Students Info’ table
## Solutions
##### 1. To create the data base named “Students Record”
   I used the syntax:
  _CREATE Database database_name_
       i.e 
 CREATE Database Student_Records; 
 
![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/Creating%20a%20database.png)
##### 2. To Create the following tables in the database:
   - Students Info  (Student ID, Gender, Name, Age, Subject)
   - Health records (Student ID, Blood Group, Height, Weight)
   - Performance (Student ID, Score, Grade)

 i. I used the syntax: CREATE Table table_name ( column1 datatype,  column2 datatype , .... );
 
 ii. To populate a table with values:
 ######  Syntax: INSERT INTO table_name (column1, column2, column3, ...)
######       VALUES (value1, value2, value3, ...);

### Paying attention to questions:
##### 3. The ID has to be unique
##### 4. Where a student has no score, it should be ‘0’ by default
##### 5. Add a constraint that prevents the ID and Subject from taking null values


iii. I Added the individual constraint where required, Then inserted each column's information.

 iv.  I used the syntax: CREATE Table table_name (column1 datatype Constraint, column2 datatype, column3 datatype, column4 datatype, column5 datatype constraint);
- ###### i.e *for Student info:* CREATE Table Student_Info(Student_ID INTEGER Unique Not Null, Gender VARCHAR(50), Name VARCHAR(50), Age INTEGER, Subject VARCHAR(50) Not Null);
###### INSERT INTO Student_Info(Student_ID, Gender, Name, Age, Subject)
###### VALUES (1, 'FEMALE', 'ANNIE JOHNSON', 17, 'Mathematics'),
 ######      (2, 'MALE', 'VICTOR JOHNSON', 18, 'English'),
 ######      (3, 'MALE', 'KOMEH KORA', 20, 'Biology'),
 ######	     (4, 'FEMALE', 'TOBI JIMOH', 22, 'Chemistry'),
 ######	     (5, 'FEMALE', 'EZEKIEL SHOLA', 19, 'Physics');


![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/creating%20student_info.png)
- ######  *for Health Records:* CREATE Table Health_Records(Student_ID INTEGER Unique Not Null, Blood_Group VARCHAR(50), Height Decimal(2,1), Weight Decimal(3,1));
###### INSERT INTO Health_Records(Student_ID, Blood_Group, Height, Weight)
###### VALUES (1, 'O+', 5.4, 63.2),
######       (2, 'A', 6.2, 65.0),
######	     (3, 'AB', 5.8, 62.0),
######	     (4, 'B', 6.0, 64.3),
######	     (5, 'O-', 6.4, 68.1);
![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/creating%20health_records.png)
- ######  *for Performance:* CREATE Table Performance(Student_ID INTEGER Unique Not Null, Score INTEGER Default 0, Grade VARCHAR(50));
###### INSERT INTO Performance(Student_ID, Score, Grade)
###### VALUES (1,' ' ,'D'),
######       (2, 66, 'B'),
######	    (3, 90, 'A'),
######	    (4, 30, 'E'),
######	    (5, 58, 'C');
The *_default constraint_* allows the score column to return '0' as a value once value isn't inputted while the _unique constraint_ makes sure there is no duplicate vaues.
![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/Creating%20performance.png)

Changing column name ‘’Subject” to ‘’Course” 
###### syntax :EXEC sp_rename 'student_info.Subject', 'Course', 'Column';
![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/Renaming%20%20subject%20to%20course.png)

Dropping the “Age” column from the ‘Students Info’ table
###### syntax : ALTER Table student_info DROP COLUMN Age;
![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/dropping%20the%20column%20age.png)

## Project Objective 2
The second objective of this project is to demonstrate the utilization of SQL queries to extract specific information from the Employee and Salary tables. By executing a series of well-defined SQL commands, we aim to achieve the tasks:
1. Select the employee table and show the data where city is Mumbai and Delhi. 
2. Select the employee table where employee first name have both ‘a’ and ‘e’  in them. 
3. Subset the employee table to have employee with date of birth above 1990
4. Subset the salary table to show salaries less than 1 million and sort in an ascending order
5. Modify email column of the employee table to contain just email without ‘@gmail.com’

## Solutions
**1. Select the employee table and show the data where city is Mumbai and Delhi.** 
Filtering the Employee Table by City:
Selecting rows from the Employee table where the city is either Mumbai or Delhi.
###### Syntax: SELECT * FROM Employee WHERE City= 'Mumbai' OR City = 'Delhi';
![]()
