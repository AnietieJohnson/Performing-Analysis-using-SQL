# STUDENT RECORD DATABASE PROJECT
## Introduction
This project aims to showcase the creation and management of a database designed to store essential information. The First database named 'Student_Records' will consist of three main tables: Students Info, Health Records, and Performance. I would also dive into importing tables (Employee and Salary) into a Second database named 'Business' to extract and uncover valuable insights and patterns within the data using SQL queries. This project requires setting up databases, creating tables, importing tables, defining constraints, and making modifications as required.
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
   A. Change column name ‘’Subject” to ‘’Course” 
   B. Drop the “Age” column from the ‘Students Info’ table
## Concept Demonstrated
- Creating a Database and Tables
- Defining Table Columns
- Use of Constraints
- Modifying Columns
- Dropping Columns

Through this task, I showcased my understanding of database design principles, constraints, data manipulation, and the ability to modify table structures. These concepts form the foundation of SQL-based data management and analysis, reflecting a key set of skills in the realm of relational databases.
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

**_Paying attention to questions:_**
##### 3. The ID has to be unique
##### 4. Where a student has no score, it should be ‘0’ by default
##### 5. Add a constraint that prevents the ID and Subject from taking null values

iii. I Added the individual constraint where required.

 iv.  Then inserted each column's information 
 ###### I used the syntax: CREATE Table table_name (column1 datatype Constraint, column2 datatype, column3 datatype, column4 datatype, column5 datatype constraint);
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

**6A. Changing column name ‘’Subject” to ‘’Course”** 
###### syntax :EXEC sp_rename 'student_info.Subject', 'Course', 'Column';
![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/Renaming%20%20subject%20to%20course.png)

**6B. Dropping the “Age” column from the ‘Students Info’ table**
###### syntax : ALTER Table student_info DROP COLUMN Age;
![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/dropping%20the%20column%20age.png)


## Project Objective 2
The second objective of this project is to demonstrate the utilization of SQL queries to extract specific information from the Employee and Salary tables. By executing a series of well-defined SQL commands, we aim to achieve the tasks:
1. Select the employee table and show the data where city is Mumbai and Delhi. 
2. Select the employee table where employee first name have both ‘a’ and ‘e’  in them. 
3. Subset the employee table to have employee with date of birth above 1990
4. Subset the salary table to show salaries less than 1 million and sort in an ascending order
5. Modify email column of the employee table to contain just email without ‘@gmail.com’
## Concept Demonstrated
- Use of the SELECT Statement
- Filtering with WHERE Clause
- String Manipulation with LIKE Operator
- Date Comparison
- Sorting Data with ORDER BY Clause

Updating Data with UPDATE Statement
Collectively, this task showcase my proficiency in querying and manipulating data using SQL. I demonstrated the ability to retrieve specific data subsets, filter rows based on conditions, work with patterns in strings, compare dates, sort data, and perform data updates. These skills are crucial for effective data analysis and management using SQL

## Solutions
**1. Select the employee table and show the data where city is Mumbai and Delhi.**
- Filtering the Employee Table by City
- Selecting rows from the Employee table where the city is either Mumbai or Delhi.
  ###### Syntax: SELECT * FROM Employee WHERE City= 'Mumbai' OR City = 'Delhi';
![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/employee%20in%20mumbai%20or%20delhi.png)
**2. Select the employee table where employee first name have both ‘a’ and ‘e’  in them.**
- Filtering the Employee Table by First Name Pattern (Firtname column here is "name")
- Extracting rows from the Employee table where the first name contains both 'a' and 'e'
  ###### Syntax: SELECT * FROM Employee WHERE name LIKE '%ae%';
![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/employees%20having%20a%20%26%20e%20in%20their%20first%20name.png)

**3. Subset the employee table to have employee with date of birth above 1990**
- Creating a subset of the Employee table to include only those employees born after the year 1990.
  ###### Syntax: SELECT * FROM Employee WHERE date_of_birth >'1990-12-31';
  ![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/employee%20with%20date%20of%20birth%20above%201990.png)
**4. Subset the salary table to show salaries less than 1 million and sort in an ascending order** 
- Extracting rows from the Salary table where the salary is less than 1 million and sorting them in ascending order.
  ###### Syntax:SELECT * FROM Salary WHERE Base <1000000 ORDER BY bASE ASC;
  ![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/salaries%20above%201M%20order%20by%20ASC.png)

**5. Modify email column of the employee table to contain just email without ‘@gmail.com’**
- Altering the email column in the Employee table to retain only the email addresses without the domain ('@gmail.com').
  ###### Syntax:UPDATE Employee
   ###### SET email = SUBSTRING(email, 1, CHARINDEX('@', email) - 1)
    ###### WHERE CHARINDEX('@', email) > 0;
  
  Before removing '@gmail.com'                 
![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/before%20%20removing%20'%40gmail'.png)

   After Removing '@gmail.com
![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/after%20update%2C%20removing%20'%40gmail.com'.png)

## Project Objective 3
The third objective ofthis project, our main objectives are to:
1. Determine the total number of employees in the Employee table.
2. Identify the top 5 cities with the highest employee counts and filter this list to include only cities with more than 15 employees.
3. Uncover the most frequently used pin codes by employees, revealing the pin codes that are utilized the most.
## Concept Demonstrated
- Aggregation with COUNT Function
- Aggregation and Filtering with GROUP BY and HAVING Clauses
- Aggregation and Sorting with ORDER BY
- Aggregation and Sorting with ORDER BY
- Subqueries and Joins
- Data Analysis and Decision Making
## Solutions
**1. Determine the total number of employees in the Employee table.**
- We begin by determining the total number of employees in our dataset. This foundational query sets the stage for further analysis and provides a clear understanding of the dataset's scale.
###### Syntax: SELECT COUNT(empID) FROM Employee
![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/Count%20of%20Employee.png)

**2. Identify the top 5 cities with the highest employee counts and filter this list to include only cities with more than 15 employees.**
- Our journey continues as we identify the top 5 cities with the highest number of employees. This initial list is then refined to spotlight cities with more than 15 employees, offering insights into where our workforce is concentrated.
###### Syntax: SELECT Top 5 city, COUNT (City) AS total_Employee FROM Employee
###### GROUP BY city
###### ORDER BY COUNT (City) DESC
![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/Top%205%20cities%20with%20highest%20number%20of%20employee.png)
###### Syntax for 'cities with more than 15': SELECT Top 5 city, COUNT (City) AS total_Employee FROM Employee
###### GROUP BY city
###### Having COUNT (City) >15
###### ORDER BY COUNT (City) DESC
![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/having%20%20greaterthan%2015.png)

**3. Uncover the most frequently used pin codes by employees, revealing the pin codes that are utilized the most.**
- Our final destination in this exploration involves unraveling the pin code puzzle. By pinpointing the most frequently used pin codes, we gain insights into the areas where employees are most active and possibly uncover trends related to commuting and residential preferences.
- First I identified the number of employees using each pincode, Then I identified the TOP 1(most used)
###### Syntax: SELECT pincode, COUNT(PINCODE) FROM Employee
###### GROUP BY pincode
###### ORDER BY COUNT(PINCODE) DESC
![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/number%20of%20employee%20using%20a%20%20code.png)
###### Syntax 'For most used pincode: SELECT Top 1 pincode, COUNT(PINCODE) FROM Employee
###### GROUP BY pincode
###### ORDER BY COUNT(PINCODE) DESC
![](https://github.com/AnietieJohnson/Performing-Analysis-using-SQL/blob/main/pincode%20used%20the%20most.png)

## Conclusion
In this project, I embarked on a comprehensive journey of data exploration and analysis using SQL queries on our employee dataset. Through exploring the provided SQL scripts, I learned the art of querying databases, filtering data, and extracting actionable insights. Overall, these tasks showcase my ability to perform data analysis using SQL, including aggregation, grouping, sorting, and potentially utilizing subqueries to retrieve and analyze data from multiple tables. These concepts are essential when working with databases and performing data-driven decision-making.



