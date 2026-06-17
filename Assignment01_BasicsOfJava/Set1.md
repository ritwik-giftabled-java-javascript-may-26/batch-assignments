## Important Steps to Follow:-  
- Clone your "name-assignments" repository.
- Create a folder named Assignment01_BasicsOfJava.
- Inside Assignment01_BasicsOfJava, create a folder named Set1.
- Inside Set1, create a Java file named SimpleInterestCalculator.java.
- Write the solution and save the file.
- Execute the following Git commands:
  - git add .
  - git commit -m "Completed Assignment01 Set1 - Simple Interest Calculator"
  - git push
- Expected Folder Structure
  - Assignment01_BasicsOfJava/Set1/SimpleInterestCalculator.java
- Expected Path
  - Assignment01_BasicsOfJava/Set1/SimpleInterestCalculator.java

# Question 1

# Simple Interest Calculator
You are building a simple interest calculator for a bank. The program will capture customer details and calculate the interest using basic arithmetic operations.

## Problem Statement:
Write a Java program that:
Accepts the following inputs:
- Account Number (int)
- Customer Name (String)
- Account Active Status (boolean – true/false)
- Principal Amount (double)
- Rate of Interest (double)
- Time in Years (int)

### Computes:
Simple Interest = (Principal × Rate × Time) / 100

### Displays:
- Account and Customer details
- All inputs and the calculated interest

### Sample Input:
Enter account number: 10123  
Enter customer name: Alice  
Is account active (true/false): true  
Enter principal amount: 15000  
Enter rate of interest: 6.5  
Enter time (in years): 2  

### Sample Output:
Interest Details:  
Account No: 10123  
Customer Name: Alice  
Account Active: true  
Principal Amount: 15000.0  
Rate of Interest: 6.5%  
Time (years): 2  
Simple Interest: 1950.0  

### Constraints:
- Use the class name as SimpleInterestCalculator
- Use the following variable names exactly:
  - accountNumber (int)
  - customerName (String)
  - isActive (boolean)
  - principal (double)
  - rate (double)
  - time (int)
  - interest (double)
- Ensure outputs follow the same structure and format as shown in the sample output (including order and percentage sign).  
- Decimal formatting also needs to be taken care of.

# Question 2

## Steps to follow:-  
Inside the folder "Assignment01_BasicsOfJava/Set1", create a Java file named StudentReportCardGenerator.java, write the solution, save it, and then do git add, commit, and push.  
**Path:-** Assignment01_BasicsOfJava/Set1/StudentReportCardGenerator.java

# Student Report Card Generator
You are developing a basic report card generator for a college's internal system. The system should accept student details and marks for three subjects, then compute the result summary using conditional logic and modular methods.  

## Problem Statement:  
Write a Java program that:  
Accepts the following student details:  
- Name (String)  
- Roll Number (int)  
- Marks for 3 subjects (int values out of 100)  

### Computes:  
Total Marks  
Average Marks  
Grade based on average  
Pass/Fail Status: A student is considered passed only if they score at least 40 marks in all three subjects  

### Displays a formatted report card with the following details:  
Name  
Roll number  
Subject marks  
Total, Average, Grade  
Final Result PASS or FAIL  

### Grading Criteria:  
| Average Marks | Grade |
| ------------- | ----- |
| 90-100 | A |
| 80-89 | B |
| 70-79 | C |
| 60-69 | D |
| Below 60 | F |
  
**Fail override rule:** If any individual subject has < 40 marks, the result is FAIL and grade is F even if the average is 60+  

### Sample Input:  
Enter student name: John  
Enter roll number: 23  
Enter marks for 3 subjects (out of 100):  
Subject 1: 85  
Subject 2: 78  
Subject 3: 92  

### Sample Output:  
--Report Card--  
Name: John  
Roll No: 23  
Marks: 85, 78, 92 Total: 255  
Average: 85.00  
Grade: B  
Result: PASS  

### Constraints:  
- The class name should be GradingSystem.
- Implement and use the following exact method signatures:
  - public static int calculate Total(int ml, int m2, int m3)
  - public static double calculateAverage (int total)
  - public static char calculateGrade(double average)
  - public static boolean isPass(int ml, int m2, int m3)
  - public static void printReport(String name, int roll, int ml, int m2, int m3, int total, double average, char grade, boolean isPassed)
- Input must be taken using Scanner class.
- Format the average up to 2 decimal places in the output.

# Question 3

## Steps to follow:-  
Inside the folder "Assignment01_BasicsOfJava/Set1", create a Java file named ElectricityBillCalculator.java, write the solution, save it, and then do git add, commit, and push.  
**Path:-** Assignment01_BasicsOfJava/Set1/ElectricityBillCalculator.java

# Electricity Bill Calculator

## Problem Statement:  
You are building an electricity billing system for a local utility provider. Based on the number of units consumed, a different rate per unit is applied. Your task is to calculate the final bill amount using methods and conditional statements.  

### Billing Rules:  
Units Consumed - Rate per Unit  
0-100 - Rs1.5  
101-300 - Rs2.5  
301-500-Rs4.0  
Above 500 - Rs6.0  

**The applicable rate is based on the total units falling into a single slab - billing is not cumulative across slabs.**  

### Sample Input:  
Enter Customer ID: 1024  
Enter Customer Name: Rahul  
Enter Units Consumed: 275  

### Sample Output:  
Electricity Bill:  
Customer ID: 1024  
Customer Name: Rahul  
Units Consumed: 275  
Total Bill: Rs687.50  

### Constraints:  
- The class name must be: ElectricityBillCalculator  
- You must create a method named calculateBill(int units) that returns a double  
- Use the following variable names exactly in your program:
  - customerld (int)
  - customerName (String)
  - units (int)
  - billAmount (double)
- Read all input using the Scanner class
- The total bill amount displayed must be rounded to 2 decimal places
