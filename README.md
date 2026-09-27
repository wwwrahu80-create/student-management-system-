# student-management-system-

CREATE DATABASE student_management;

USE student_management;

-- Create Students table
CREATE TABLE Students (
    Student_ID INT PRIMARY KEY,
    Name VARCHAR(50),
    Age INT,
    Gender VARCHAR(10),
    Course VARCHAR(50),
    Marks INT
);

-- Insert student data
INSERT INTO Students VALUES
(1, 'Anu', 20, 'Female', 'BSc Computer Science', 85),
(2, 'Rahul', 21, 'Male', 'BSc Mathematics', 78),
(3, 'Jessie', 20, 'Female', 'BSc Computer Science', 92),
(4, 'Chethan', 22, 'Male', 'BSc Mathematics', 67),
(5, 'Messie', 21, 'Female', 'BSc Computer Science', 88);

-- Display all students
SELECT * FROM Students;

-- Find students who scored more than 80
SELECT * FROM Students
WHERE Marks > 80;

-- Find the highest marks
SELECT MAX(Marks) AS Highest_Marks
FROM Students;

-- Find the average marks
SELECT AVG(Marks) AS Average_Marks
FROM Students;

-- Count total students
SELECT COUNT(*) AS Total_Students
FROM Students;

-- Display students in Computer Science
SELECT * FROM Students
WHERE Course = 'BSc Computer Science';

-- Display students from highest to lowest marks
SELECT * FROM Students
ORDER BY Marks DESC;