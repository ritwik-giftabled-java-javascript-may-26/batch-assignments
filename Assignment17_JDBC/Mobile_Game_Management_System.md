# Mobile Game Management System

Develop a Mobile Game Management System in Java that performs CRUD operations on a mobile game database table using JDBC and MySQL.  

## Database Details
- Table Name: mobile_game_data
- Database URL: jdbc:mysql://localhost/giftabled
- Username: <your_database_username>
- Password: <your_database_password>

## Table Structure
| Column Name | Data Type |
| ----------- | --------- |
| id | INT (Primary Key) |
| game_name | VARCHAR(100) |
| developer | VARCHAR(100) |
| downloads | DOUBLE |
| rating | INT |

## Class Requirements
- Main Class: MobileGameManagementSystem
- Use static final constants for DB credentials
- Use Scanner for input (with try-with-resources)
- Use PreparedStatement for all database operations

## Functional Requirements  
1. Add Mobile Game Record  
Insert a new mobile game record (id, game_name, developer, downloads, rating) into the database.  
After insertion, display all records sorted by downloads in descending order.  
Print:  
Mobile game data added successfully.  
on successful insertion.  

3. Delete Games by Rating  
Read a rating limit value from the user.  
Delete all mobile game records where the rating is less than the given limit.  
After deletion, display:  
<count> game(s) deleted where Rating <<limit>.   
Then display remaining records sorted by downloads in descending order under the header:   
All Records After Deletion:  

5. Update Game Downloads   
Increase the downloads by 500000 for all games where the second character of the developer name is a vowel (a, e, i, o, u-case-insensitive).  
After updating, display:  
<count> record(s) updated successfully.  
Then display all records sorted by downloads in descending order under the header:  
All Records After Update (Sorted by Downloads DESC):  

7. Display All Mobile Games  
Retrieve and display all mobile game records sorted by downloads in descending order.  

9. Invalid Operation  
If the user enters an invalid operation number, display:  
Invalid operation number  
Display Format  
ID: <id>, Game: <game_name>, Developer: <developer>, Downloads: <downloads>, Rating: <rating>  

## Sample Input and Output
### Sample Input 1 - Add Mobile Game
1  
6  
Free Fire  
Garena  
8500000  
5  

### Sample Output 1
Mobile game data added successfully.  
ID: 6, Game: Free Fire, Developer: Garena, Downloads: 8500000.0, Rating: 5   
ID: 3, Game: BGMI, Developer: Krafton, Downloads: 7000000.0, Rating: 5   
ID: 2, Game: Clash Royale, Developer: Supercell, Downloads: 6500000.0, Rating: 4   
ID: 4, Game: Asphalt 9, Developer: Gameloft, Downloads: 5500000.0, Rating: 4   
ID: 1, Game: Subway Surfers, Developer: SYBO, Downloads: 5000000.0, Rating: 5   
ID: 5, Game: Temple Run, Developer: Imangi, Downloads: 4000000.0, Rating: 3  

### Sample Input 2 - Update Downloads
2

### Sample Output 2
3 record(s) updated successfully.  
All Records After Update (Sorted by Downloads DESC):  
ID: 6, Game: Free Fire, Developer: Garena, Downloads: 9000000.0, Rating: 5   
ID: 3, Game: BGMI, Developer: Krafton, Downloads: 7500000.0, Rating: 5  
ID: 2, Game: Clash Royale, Developer: Supercell, Downloads: 6500000.0, Rating: 4   
ID: 4, Game: Asphalt 9, Developer: Gameloft, Downloads: 6000000.0, Rating: 4   
ID: 1, Game: Subway Surfers, Developer: SYBO, Downloads: 5000000.0, Rating: 5   
ID: 5, Game: Temple Run, Developer: Imangi, Downloads: 4000000.0, Rating: 3  

### Sample Input 3 - Delete by Rating
3  
4  

### Sample Output 3
1 game(s) deleted where Rating < 4.  
All Records After Deletion:  
ID: 6, Game: Free Fire, Developer: Garena, Downloads: 9000000.0, Rating: 5   
ID: 3, Game: BGMI, Developer: Krafton, Downloads: 7500000.0, Rating: 5  
ID: 2, Game: Clash Royale, Developer: Supercell, Downloads: 6500000.0, Rating: 4   
ID: 4, Game: Asphalt 9, Developer: Gameloft, Downloads: 6000000.0, Rating: 4   
ID: 1, Game: Subway Surfers, Developer: SYBO, Downloads: 5000000.0, Rating: 5  

### Sample Input 4 - Display All Games  
4  

### Sample Output 4  
ID: 6, Game: Free Fire, Developer: Garena, Downloads: 9000000.0, Rating: 5   
ID: 3, Game: BGMI, Developer: Krafton, Downloads: 7500000.0, Rating: 5   
ID: 2, Game: Clash Royale, Developer: Supercell, Downloads: 6500000.0, Rating: 4   
ID: 4, Game: Asphalt 9, Developer: Gameloft, Downloads: 6000000.0, Rating: 4   
ID: 1, Game: Subway Surfers, Developer: SYBO, Downloads: 5000000.0, Rating: 5  

### Sample Input 5 - Invalid Operation
9  

### Sample Output 5
Invalid operation number  
