# Content Management System 

## Overview
The Content Management System is designed to manage and schedule various learning contents efficiently. It allows adding, updating, deleting, and displaying content records. The records are always displayed sorted in ascending order of time spent, and then by content_name, providing a better organized view.  

## Table Structure
Table Name: content

| Column Name | Data Type |
| ----------- | --------- |
| content_id | INT |
| content_name | VARCHAR(100) |
| completion_percentage | DOUBLE |
| time_spent | DOUBLE |
| content_created_date | VARCHAR(20) |
| content_description | VARCHAR(255) |

## Constraints
- Class Name: Content ManagementSystem
- Database Table Name: content (case-sensitive)
- Database URL: jdbc:mysql://localhost/giftabled
- Username: <your_database_username>
- Password: <your_database_password>
- JDBC Driver: com.mysql.cj.jdbc.Driver

## Methods to be implemented
- public static Connection getConnection()  
- public static void displayContentByThreshold (Connection con, Scanner sc)
- public static void insertContent (Connection con, Scanner sc)
- public static void updateCompletion Percentage (Connection con, Scanner sc)
- public static void deleteContent (Connection con, Scanner sc)
- public static void processMenu (Connection con, Scanner sc)

## Requirements
The program should support the following operations based on user choice:  

### Insert New Content   
Input: content_id, content_name, completion_percentage, time spent, content_created_date, content_description.   
Insert a new content record into the table.  

After insertion, print:  
Content added successfully!  
And display the records in the table  

### Update Content
Input:  
content_name  
New completion_percentage.  
Find contents where the content_name matches the given input and update their completion_percentage to the new value.   

After updating, print:   
Completion percentage updated successfully!  
And display the records in the table  

### Delete Content
Input: Start word, End word.  
Delete contents where content_description starts with the given start word OR ends with the given end word.  

After deletion, print:  
Content deleted successfully!  
And display the records in the table  

### Display All Contents
Input: completion_percentage threshold, limit count.  
Display content_name, time spent, and completion_percentage for contents where completion_percentage is above the threshold.  
Display only up to the specified limit and in descending order by time spent.  

## Input Format
Choice (1/2/3/4)  

For Choice 1  
content_id  
content_name  
completion_percentage  
time_spent  
content_created_date  
content_description  
  
For Choice 2  
content_name  
new_completion_percentage  
  
For Choice 3   
start_word  
end_word  
  
For Choice 4  
completion_percentage threshold  
limit count  
  
## Output Format  
Insert Success   
Content added successfully!  
Contentld: <content_id>, ContentName: <content_name>, Completion Percentage: <completion_percentage>, TimeSpent: <time_spent>, ContentCreatedDate: <content_created_date>, ContentDescription: <content_description> 
  
Update Success  
Completion percentage updated successfully!  
Contentld: <content_id>, ContentName: <content_name>, CompletionPercentage: <completion_percentage>, TimeSpent: <time_spent>, ContentCreated Date: <content_created_date>, ContentDescription: <content_description>  
  
Delete Success  
Content deleted successfully!  
Contentld: <content_id>, ContentName: <content_name>, Completion Percentage: <completion_percentage>, TimeSpent: <time_spent>, ContentCreated Date: <content_created_date>, ContentDescription: <content_description>  
  
Display  
ContentName: <content_name>, TimeSpent: <time_spent>, Completion Percentage: <completion_percentage>  
  
## Sample Inputs & Outputs
### Sample Input 1:  
1  
207  
Machine Learning  
75.0  
8.5  
2024-09-27  
Introduction to Machine Learning concepts    

### Sample Output 1:  
Content added successfully!  
Contentld: 205, ContentName: Software Testing, CompletionPercentage: 95.0, TimeSpent: 4.5, ContentCreated Date: 2024-10-03, ContentDescription: Principles of software   
Contentld: 202, ContentName: SQL Basics, CompletionPercentage: 60.0, TimeSpent: 5.0, ContentCreated Date: 2024-09-27, ContentDescription: SQL operations and queries   
Contentld: 204, ContentName: Agile Methodology, Completion Percentage: 70.75, TimeSpent: 6.5, ContentCreated Date: 2024-10-01, ContentDescription: Agile practices and framework   
Contentld: 201, ContentName: Java Basics, CompletionPercentage: 80.5, TimeSpent: 7.25, ContentCreated Date: 2024-09-25, ContentDescription: Introduction to Java fundamentals   
Contentld: 207, ContentName: Machine Learning, Completion Percentage: 75.0, TimeSpent: 8.5, ContentCreated Date: 2024-09-27, ContentDescription: Introduction to Machine Learning concepts   
Contentld: 203, ContentName: Data Structures, Completion Percentage: 90.25, TimeSpent: 10.0, ContentCreated Date: 2024-09-30, ContentDescription: Introduction to data structures  
  
### Sample Input 2  
2  
Data Structures  
85.25  
  
### Sample Output 2  
Completion percentage updated successfully!  
Contentld: 205, ContentName: Software Testing, Completion Percentage: 95.0, TimeSpent: 4.5, ContentCreated Date: 2024-10-03, ContentDescription: Principles of software   
Contentld: 202, ContentName: SQL Basics, CompletionPercentage: 60.0, TimeSpent: 5.0, ContentCreatedDate: 2024-09-27, ContentDescription: SQL operations and queries   
Contentld: 204, ContentName: Agile Methodology, Completion Percentage: 70.75, TimeSpent: 6.5, ContentCreated Date: 2024-10-01, ContentDescription: Agile practices and framework  
Contentld: 201, ContentName: Java Basics, CompletionPercentage: 80.5, TimeSpent: 7.25, ContentCreated Date: 2024-09-25, ContentDescription: Introduction to Java fundamentals   
Contentld: 207, ContentName: Machine Learning, CompletionPercentage: 75.0, TimeSpent: 8.5, ContentCreated Date: 2024-09-27, ContentDescription: Introduction to Machine Learning concepts   
Contentld: 203, ContentName: Data Structures, CompletionPercentage: 85.25, TimeSpent: 10.0, ContentCreated Date: 2024-09-30, ContentDescription: Introduction to data structures  
  
### Sample Input 3  
3  
Introduction  
fundamentals  

### Sample Output 3  
Content deleted successfully!  
Contentld: 205, ContentName: Software Testing, CompletionPercentage: 95.0, TimeSpent: 4.5, ContentCreated Date: 2024-10-03, ContentDescription: Principles of software   
Contentld: 202, ContentName: SQL Basics, CompletionPercentage: 60.0, TimeSpent: 5.0, ContentCreated Date: 2024-09-27, ContentDescription: SQL operations and queries   
Contentld: 204, ContentName: Agile Methodology, Completion Percentage: 70.75, TimeSpent: 6.5, ContentCreated Date: 2024-10-01, ContentDescription: Agile practices and framework  
  
### Sample Input 4  
4  
70.0 3  
  
### Sample Output 4  
ContentName: Agile Methodology, TimeSpent: 6.5, CompletionPercentage: 70.75 ContentName: Software Testing, TimeSpent: 4.5, CompletionPercentage: 95.0  
  
### Sample Input 5  
6  
  
### Sample Output 5  
Invalid Choice  
