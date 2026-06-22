# Aggregation Hands-on Practice

## Use the following collection:

db.students.insertMany([

{name:"Rahul",city:"Delhi",course:"Java",marks:85,age:22},

{name:"Amit",city:"Mumbai",course:"Python",marks:91,age:24},

{name:"Sneha",city:"Delhi",course:"Java",marks:78,age:21},

{name:"Riya",city:"Kolkata",course:"React",marks:88,age:23},

{name:"Karan",city:"Delhi",course:"Python",marks:72,age:25},

{name:"Neha",city:"Mumbai",course:"Java",marks:95,age:24},

{name:"Arjun",city:"Delhi",course:"React",marks:81,age:22},

{name:"Priya",city:"Mumbai",course:"Java",marks:84,age:23},

{name:"Vikas",city:"Pune",course:"Python",marks:76,age:26},

{name:"Ananya",city:"Kolkata",course:"React",marks:92,age:22}

]);  

- Exercise 1 – $match  
Find all Java students.  

- Exercise 2 – $match  
Find students with marks greater than 85.  

- Exercise 3 – $project  
Display only name, course, and marks (exclude _id).  

- Exercise 4 – $project  
Rename name to studentName and marks to score.  

- Exercise 5 – $sort  
Display students in descending order of marks.  

- Exercise 6 – $limit  
Show the top 5 highest-scoring students.  

- Exercise 7 – $group  
Count the number of students in each city.  

**Expected Output**  
| City | Students |
| ---- | -------- |
| Delhi	| 4 |
| Mumbai | 3 |
| Kolkata	| 2 |
| Pune | 1 |

- Exercise 8 – $group  
Find the average marks for each course.  

- Exercise 9 – $group  
Find the highest marks achieved in each course.  

- Exercise 10 – $group  
Find the lowest marks achieved in each course.  

- Exercise 11 – $group  
Calculate the total marks obtained by students in each city.  

- Exercise 12 – $group + $push  
Create an array of student names grouped by course.  

- Exercise 13 – $count  
Count how many students have marks greater than or equal to 80.  

- Exercise 14 – $addFields  
Add a new field graceMarks with value 5.  

- Exercise 15 – $addFields  
Create a finalMarks field by adding 5 to marks.  

- Exercise 16 – Multi-stage Pipeline  
Display the top 3 Java students with the highest marks, showing only their names and marks.  

**Pipeline Hint:**  

$match  
    ↓  
$sort  
    ↓  
$limit  
    ↓  
$project  

- Exercise 17 – Dashboard Report  
Generate a report showing, for each course:  
  - Number of students
  - Average marks
  - Highest marks
  - Lowest marks

*Hint:* Use a single $group stage with multiple accumulators ($sum, $avg, $max, $min).  

- Exercise 18 – Dashboard Report  
Find the city with the highest average marks.  

*Hint:* Use:  

$group  
   ↓  
$sort  
   ↓  
$limit  
