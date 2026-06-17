# Question 1

## Important Steps to Follow:-  
- Clone your "name-assignments" repository.
- Inside Assignment01_BasicsOfJava folder, create a folder named Set2.
- Inside Set2, create a Java file named SumOfNaturalNumbers.java.
- Write the solution and save the file.
- Execute the following Git commands:
  - git add .
  - git commit -m "Completed Assignment01 Set2 - Sum Of Natural Numbers"
  - git push
- Expected Folder Structure/Path  
  - Assignment01_BasicsOfJava/Set2/SumOfNaturalNumbers.java

# Sum of Natural Numbers  

## Problem Statement:
Write a Java program that takes a positive integer n as input and calculates the sum of the first n natural numbers using a loop.  

### Sample Input:  
Enter a positive integer: 10  

### Sample Output:  
Sum of first 10 natural numbers is: 55  

### Constraints:  
- Class name: SumNaturalNumbers
- Use for loop to calculate the sum
- Use variable names exactly: n (int) input number
- sum (int) - sum of numbers
- Input must be read using Scanner

# Question 2

## Steps to follow:-  
Inside the folder "Assignment01_BasicsOfJava/Set2", create a Java file named CountDigitsInANumber.java, write the solution, save it, and then do git add, commit, and push.  
**Path:-** Assignment01_BasicsOfJava/Set2/CountDigitsInANumber.java

# Count Digits in a Number  

## Problem Statement:
Write a Java program that reads an integer from the user and counts the number of digits in the integer using a while loop inside a user-defined method.  

### Details:  
- Create a method countDigits (int number) that returns the count of digits.  
- Use a while loop to count the digits.  
- Handle negative numbers by considering their absolute value.  
- Print the count in the main method.  

### Sample Input:  
Enter an integer: 45982  

### Sample Output:  
Number of digits in 45982 is: 5  

# Question 3

## Steps to follow:-  
Inside the folder "Assignment01_BasicsOfJava/Set2", create a Java file named CafeteriaBillingSystem.java, write the solution, save it, and then do git add, commit, and push.  
**Path:-** Assignment01_BasicsOfJava/Set2/CafeteriaBillingSystem.java

# Cafeteria Billing System Problem Statement:
You are building a simple Cafeteria Billing System. 
- Display a menu with item numbers and prices.
- Let the user select an item by entering its number and provide the quantity.
- Repeat this process until the user enters 0 to finish.
- For each selection, calculate the subtotal using a method and add it to the total bill.
- Use a do-while loop to repeat the process.

### Fixed Menu:
1. Coffee - Rs 50  
2. Sandwich - Rs 70  
3. Burger - Rs 100  
O. Exit  

### Sample Input:  
Enter item number (0 to finish): 1  
Enter quantity: 2  
Enter item number (0 to finish): 2  
Enter quantity: 1  
Enter item number (0 to finish): 0  

### Sample Output:    
Subtotal for Coffee (x2): Rs100.0  
Subtotal for Sandwich (x1): Rs70.0  
Total Bill: Rs170.00  

### Constraints:
- Class name: CafeteriaBillingSystem
- Method signature: public static double calculateSubtotal(int itemNumber, int quantity)
- Use variable names:
  - itemNumber (int)
  - quantity (int)
  - subtotal (double)
  - totalBill (double)
- Use a do-while loop to repeat the item entry.
- Use System.out.printf() to print the total bill rounded to 2 decimal places.
