# Online Fitness Class Management System 

## Overview
The Online Fitness Class Management System is designed to manage and schedule fitness classes efficiently. It allows adding, updating, deleting, and displaying class records. The records are always displayed sorted in reverse alphabetical order of the class type, providing a better organized view.

## Table Structure
| Column Name | Data Type | Description |
| ----------- | --------- | ----------- |
| class_id | INT | Primary Key |
| class_type | VARCHAR | Type of fitness class |
| class_date | DATE | Date of the class |
| instructor | VARCHAR | Name of the instructor |
| duration_mins | INT | Duration of the class |

## Constraints
- Class Name: OnlineFitnessClassManagement
- Database Table Name: fitness_class (case-sensitive)
- Database URL: jdbc:mysql://localhost/giftabled
- Username: <your_database_username>
- Password: <your_database_password>
- JDBC Driver: com.mysql.cj.jdbc.Driver

## Methods to be implemented
- public static Connection getConnection()
- public static void displayAllClasses (Connection con)
- public static void insertClass (Connection con, Scanner sc)
- public static void updateClassDuration (Connection con, Scanner sc)
- public static void deleteClass (Connection con, Scanner sc)
- public static void processMenu (Connection con, Scanner sc)

## Requirements
The program should support the following operations based on user choice:

### Insert New Fitness Class
Input: class_id, class_type, class_date, instructor, duration_mins
Insert a new class record into the table.
After insertion, print:
Fitness class added successfully!
Then, display all classes sorted in reverse alphabetical order of class_type.

### Update Class Duration
Input: class_id, class_type
Find the class with matching class_id and class_type.
Increase its duration_mins by 30 minutes.
After updating, print:
Class duration updated successfully!
Then, display all classes sorted in reverse alphabetical order of class_type.

### Delete a Fitness Class
Input: class_id
Delete the record matching the given class_id.
After deletion, print:
Fitness class deleted successfully!
Then, display all classes sorted in reverse alphabetical order of class_type.

### Display All Fitness Classes
No additional input
Simply display all classes sorted in reverse alphabetical order of class_type.

### Sorting Requirement
All class displays must be sorted in reverse alphabetical order of the class_type field.

## Notes
- Use try, catch, and finally blocks to handle SQLException properly.
- The table name must match exactly: fitness_class.
- The database table is assumed to be already created with some records (class_id range: 201 to 205). 
- Your program should work seamlessly with the provided database configuration.

## Input Format
Choice (1/2/3/4)  

For Choice 1  
class_id  
class_type  
class_date  
instructor  
duration_mins  

For Choice 2  
class_id  
class_type  

For Choice 3   
class_id  

For Choice 4  
(no further inputs)  

If you choose any other option, it should display:  
"Invalid Choice"  

## Output Format  
Insert Success  
Fitness class added successfully!  
ClassID: <id>, Type: <class_type>, Date: <class_date>, Instructor: <instructor>, Duration: <duration_mins> mins   
 
Update Success  
Class duration updated successfully!  
ClassID: <id>, Type: <class_type>, Date: <class_date>, Instructor: <instructor>, Duration: <duration_mins> mins  

Delete Success  
Fitness class deleted successfully!  
ClassID: <id>, Type: <class_type>, Date: <class_date>, Instructor: <instructor>, Duration: <duration_mins> mins  

Display  
ClassID: <id>, Type: <class_type>, Date: <class_date>, Instructor: <instructor>, Duration: <duration_mins> mins Sample Inputs and Outputs  

## Sample Inputs and Outputs   
Sample Input 1  
1  
206  
Yoga  
2025-08-10  
Anna Lee  
60  

Sample Output 1  
Fitness class added successfully!  
ClassID: 203, Type: Zumba, Date: 2025-08-18, Instructor: Lisa Ray, Duration: 55 mins  
ClassID: 206, Type: Yoga, Date: 2025-08-10, Instructor: Anna Lee, Duration: 60 mins   
ClassID: 202, Type: Spin, Date: 2025-08-12, Instructor: David Kim, Duration: 45 mins   
ClassID: 201, Type: Pilates, Date: 2025-08-15, Instructor: Emily Chen, Duration: 50 mins   
ClassID: 205, Type: Kickboxing, Date: 2025-08-20, Instructor: John Doe, Duration: 65 mins   
ClassID: 204, Type: HIIT, Date: 2025-08-22, Instructor: Mike Wong, Duration: 40 mins  

Sample Input 2  
2  
201  
Pilates  

Sample Output 2    
Class duration updated successfully!  
ClassID: 203, Type: Zumba, Date: 2025-08-18, Instructor: Lisa Ray, Duration: 55 mins   
ClassID: 202, Type: Spin, Date: 2025-08-12, Instructor: David Kim, Duration: 45 mins   
ClassID: 201, Type: Pilates, Date: 2025-08-15, Instructor: Emily Chen, Duration: 80 mins   
ClassID: 205, Type: Kickboxing, Date: 2025-08-20, Instructor: John Doe, Duration: 65 mins   
ClassID: 204, Type: HIIT, Date: 2025-08-22, Instructor: Mike Wong, Duration: 40 mins  

Sample Input 3  
3  
205  

Sample Output 3  
Fitness class deleted successfully!  
ClassID: 203, Type: Zumba, Date: 2025-08-18, Instructor: Lisa Ray, Duration: 55 mins   
ClassID: 202, Type: Spin, Date: 2025-08-12, Instructor: David Kim, Duration: 45 mins   
ClassID: 201, Type: Pilates, Date: 2025-08-15, Instructor: Emily Chen, Duration: 50 mins   
ClassID: 204, Type: HIIT, Date: 2025-08-22, Instructor: Mike Wong, Duration: 40 mins  

Sample Input 4  
4  

Sample Output 4  
ClassID: 203, Type: Zumba, Date: 2025-08-18, Instructor: Lisa Ray, Duration: 55 mins   
ClassID: 202, Type: Spin, Date: 2025-08-12, Instructor: David Kim, Duration: 45 mins   
ClassID: 201, Type: Pilates, Date: 2025-08-15, Instructor: Emily Chen, Duration: 50 mins   
ClassID: 205, Type: Kickboxing, Date: 2025-08-20, Instructor: John Doe, Duration: 65 mins   
ClassID: 204, Type: HIIT, Date: 2025-08-22, Instructor: Mike Wong, Duration: 40 mins  

Sample Input 5  
7  

Sample Output 5  
Invalid Choice  
