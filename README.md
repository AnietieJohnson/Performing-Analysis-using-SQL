# STUDENT RECORD DATABASE PROJECT
## Introduction
This project aims to showcase the creation and management of a database designed to store essential information about students. The database will consist of three main tables: Students Info, Health Records, and Performance. This project requires setting up a database, creating tables, defining constraints, and making modifications as required.
## Project Objective
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
I used the syntax: CREATE Table table_name ( column1 datatype,  column2 datatype , .... );

Paying attention to questions
##### 3. The ID has to be unique
##### 4. Where a student has no score, it should be ‘0’ by default
##### 5. Add a constraint that prevents the ID and Subject from taking null values
I Added the individual constraint where required.

I used the syntax: CREATE Table table_name (column1 datatype Constraint, column2 datatype, column3 datatype, column4 datatype, column5 datatype constraint);

i.e **for Student info:** CREATE Table Student_Info(Student_ID INTEGER Unique Not Null, Gender VARCHAR(50), Name VARCHAR(50), Age INTEGER, Subject VARCHAR(50) Not Null);

![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/creating%20student_info.png)


