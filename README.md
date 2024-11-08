# SQL Practical Assignment 

## Create database and perform all basic queries.

- **To Create Database** (CREATE & USE Query)

  `CREATE DATABASE StudentDB;`

   `USE StudentDB;`

   `CREATE TABLE students (`

     `id INT AUTO_INCREMENT PRIMARY KEY,`

     `name_ VARCHAR(100),`
                 
     `rollno VARCHAR(50),`  
               
     `enrollment_no VARCHAR(50),`  
         
     `cgpa DECIMAL(3,2),`
                   
     `subject_ VARCHAR(100),`
               
     `phone_no VARCHAR(15),`  
             
     `address VARCHAR(255),` 
              
     `date_of_birth DATE,`  
              
     `gender ENUM('Male', 'Female', 'Other')` 

  `);`
  
  *Output:*

  <img src="create table.png">
  
---

- **DROP Query**

  `DROP TABLE students;`
  
  *Output:*
  
  <img src="drop table.png">

---
  
- **INSERT Query**

`INSERT INTO students_records (name, rollno, enrollment_no, cgpa, subject, phone_no, address, date_of_birth, gender)`
`VALUES`
    `('Aarav Kumar', 'S201', 'EN2023001', 8.75, 'Computer Science', '9876543210', 'B-101, Green Park, New Delhi', '2001-05-14', 'Male'),`
    `('Sanya Gupta', 'S202', 'EN2023002', 9.22, 'Electrical Engineering', '9123456789', 'A-22, Sector 15, Noida, Uttar Pradesh', '2000-08-22', 'Female'),`
   `('Ravi Patel', 'S203', 'EN2023003', 7.59, 'Mechanical Engineering', '9555555555', 'H-234, Vaishali Nagar, Jaipur, Rajasthan', '2000-11-30', 'Male'),`
    `('Priya Sharma', 'S204', 'EN2023004', 8.19, 'Civil Engineering', '9912345678', 'Q-10, Rajendra Nagar, Patna, Bihar', '1999-06-05', 'Female'),`
    `('Arjun Yadav', 'S205', 'EN2023005', 8.63, 'Information Technology', '9654321987', 'E-45, MG Road, Bangalore, Karnataka', '2001-02-17', 'Male'),`
    `('Neha Verma', 'S206', 'EN2023006', 9.09, 'Biotechnology', '9911223344', 'D-67, Indira Nagar, Lucknow, Uttar Pradesh', '2000-03-30', 'Female'),`
    `('Vikas Singh', 'S207', 'EN2023007', 7.86, 'Chemical Engineering', '9900112233', 'A-9, Shanti Nagar, Kolkata, West Bengal', '2000-07-12', 'Male'),`
    `('Simran Kaur', 'S208', 'EN2023008', 9.50, 'Aerospace Engineering', '9988776655', 'C-12, Sector 9, Chandigarh', '1998-12-22', 'Female'),`
    `('Aditya Deshmukh', 'S209', 'EN2023009', 8.42, 'Electronics Engineering', '9977554433', 'G-23, Shivaji Nagar, Pune, Maharashtra', '2001-09-09', 'Male'),`
    `('Kavya Reddy', 'S210', 'EN2023010', 8.89, 'Civil Engineering', '9922334455', 'B-101, Jubilee Hills, Hyderabad, Telangana', '2000-04-25', 'Female');`

  
  *Output:*
  
  <img src="insert.png">

---

- **SELECT Query**

  `SELECT * FROM studentdb.students;`
  
  *Output:*
  
  <img src="select.png">

---

- **UPDATE & WHERE Query**

  `UPDATE students`
  
  `SET subject_ = 'Mechanical Engineering'`
  
  `WHERE ID = '6';`
  
  *Output:*
  
  <img src="updatewhere.png">

---

- **ALTER Query**

  `ALTER TABLE students`
  
  `CHANGE enrollment_no enroll_no VARCHAR(50);`
  
  *Output:*
  
  <img src="alter.png">

---

- **ORDER BY Query**

  `SELECT name_ , rollno, subject_`
  
  `FROM students`
  
  `ORDER BY cgpa;`
  
  *Output:*
  
  <img src="order by.png">

---

- **Inner Join Query**

  `SELECT s.name_, s.rollno, s.subject, c.course_name`
  
  `FROM students s`
  
  `INNER JOIN courses c ON s.rollno = c.rollno;`
  
  *Output:*
  
  <img src="innerjoin.png">
---

- **Left Join Query**

  `SELECT s.name_, s.rollno, s.subject_, c.course_name`
  
  `FROM students s`
 
  `LEFT JOIN courses c ON s.rollno = c.rollno;`

  
  *Output:*
  
  <img src="left join.png">

---

- **Right Join Query**

 ` SELECT c.course_name, s.name_, s.rollno`

 `FROM students s`

 `RIGHT JOIN courses c ON s.rollno = c.rollno;`


  *Output:*
  
  <img src="rightjoin.png">

---

- **Full Outer-Join Query**

`SELECT s.name_, s.rollno, c.course_name`

`FROM students s`

`LEFT JOIN courses c ON s.rollno = c.rollno`

`UNION`

`SELECT s.name_, s.rollno, c.course_name`

`FROM students s`

`RIGHT JOIN courses c ON s.rollno = c.rollno;`

 
  
  *Output:*
  
  <img src="fullouterjoin.png">

---

- **Distinct Query**

 ` SELECT DISTINCT subject_`

 `FROM students;`


  *Output:*
  
  <img src="distinct.png">
