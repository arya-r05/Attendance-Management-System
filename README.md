Attendance Management System

Project Overview

The Attendance Management System is a desktop-based application developed using **Python** and **MySQL**.
It provides a graphical interface that allows users to manage student attendance efficiently without using manual registers.

The system stores student details, subjects, and attendance records in a MySQL database and allows users to mark and track attendance easily through a Tkinter-based GUI.



Technologies Used

* **Python** – Application logic
* **Tkinter** – Graphical User Interface (GUI)
* **MySQL** – Database for storing records
* **mysql.connector** – Python library used to connect Python with MySQL



System Features

* Add new students
* Store subject details
* Mark attendance for each student and subject
* Prevent duplicate attendance entries
* View student records
* View attendance records
* Search attendance by student
* Automatically calculate attendance percentage



Database Structure

1. Student Table

Stores student information.

Fields:

* student_id (Primary Key)
* name
* department
* year

2. Subject Table

Stores subject information.

Fields:

* subject_id (Primary Key)
* subject_name

3. Attendance Table

Stores attendance records and links students with subjects.

Fields:

* attendance_id (Primary Key)
* student_id (Foreign Key)
* subject_id (Foreign Key)
* date
* status (Present / Absent)



How the System Works

1. The user opens the application interface.
2. Students are added to the system using the **Add Student** option.
3. Subjects are stored in the subject table.
4. When marking attendance:

   * The user selects a student.
   * The user selects a subject.
   * The user enters the date and attendance status.
5. The system saves the record in the **attendance table**.
6. Before saving, the system checks if attendance for the same student, subject, and date already exists to prevent duplicates.



Attendance Percentage Calculation

The attendance percentage is calculated dynamically using the formula:

Attendance Percentage = (Total Present Classes / Total Classes) × 100

Example:
If a student attended 8 classes out of 10:

Percentage = (8 / 10) × 100 = 80%

The system uses SQL COUNT queries to calculate the total number of classes and present classes.







Project Purpose

The aim of this project is to replace the traditional manual attendance system with a digital solution that is faster, more accurate, and easier to manage.



Author

Student Mini Project – Attendance Management System using Python and MySQL.
