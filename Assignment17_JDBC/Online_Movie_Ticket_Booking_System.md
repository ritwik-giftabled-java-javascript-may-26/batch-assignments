# Online Movie Ticket Booking System

## Overview
The Online Movie Ticket Booking System is designed to manage and streamline movie show bookings efficiently. It allows adding new movie show records, updating available seats, deleting shows, and displaying all shows.  
All show records must be displayed in descending order of available seats, so users can easily see shows with the most available seats first.  

## Table Structure
Table name: movie_show
| Column Name | Data Type | Description |
| ----------- | --------- | ----------- |
| show_id | INT | Primary key, unique show ID |
| movie_title | VARCHAR(100) | Title of the movie |
| show_date | VARCHAR(20) | Date of the show |
| theater_name | VARCHAR(100) | Name of the theater |
| available seats | INT | Number of available seats |

## Constraints
- Class Name: OnlineMovieTicketBooking
- Database Table Name: movie_show (case-sensitive)
- Database URL: jdbc:mysql://localhost/giftabled
- Username: <your-database-username>
- Password: <your-database-password>
- JDBC Driver: com.mysql.cj.jdbc.Driver
  
## Methods to be implemented
- public static Connection getConnection()
- public static void displayAllShows (Connection con)
- public static void insertShow (Connection con, Scanner sc)
- public static void updateSeats (Connection con, Scanner sc)
- public static void deleteShow (Connection con, Scanner sc)
- public static void processMenu (Connection con, Scanner sc)

## Requirements
Insert New Movie Show  
Input: show_id, movie_title, show_date, theater_name, available_seats  
Insert a new show record into the table.  
After insertion, print:  
Movie show added successfully!  
Then display all shows sorted in descending order of available_seats.  

Update Available Seats  
Input:  
show_id  
movie_title 

Operation:  
Finds the show with matching show_id and movie_title, then increases available_seats by 20.  

Delete Movie Show
Input:  
show_id   
movie_title  

Operation:  
Deletes the movie show that matches both show_id and movie_title. After deletion, print:  
Movie show deleted successfully!  
Then display all shows sorted in descending order of available_seats.  

Display All Shows  
Display all shows sorted in descending order of available_seats.  

Sorting Requirement  
All show displays must be sorted in descending order of the available seats field, so that shows with the most seats available appear first.  

## Input Format
Choice (1/2/3/4)  

For Choice 1  
show_id  
movie_title  
show_date  
theater_name  
available seats  

For Choice 2  
show_id  
movie_title  

For Choice 3  
show_id  

For Choice 4  
(no further inputs)  

If you choose any other option, it should display:  
"Invalid Choice"  

## Output Format
Insert Success  
Movie show added successfully!  
ShowID: <id>, Movie: <movie_title>, Date: <show_date>, Theater: <theater_name>, Available Seats: < available_seats>  
Update Success  
Seats updated successfully!  
ShowID: <id>, Movie: <movie_title>, Date: <show_date>, Theater: <theater_name>, Available Seats: <available_seats>  
Delete Success  
Movie show deleted successfully!  
ShowID: <id>, Movie: <movie_title>, Date: <show_date>, Theater: <theater_name>, Available Seats: < available_seats>  
Display  
ShowID: <id>, Movie: <movie_title>, Date: <show_date>, Theater: <theater_name>, Available Seats: <available_seats>  

## Sample Inputs and Outputs
Sample Input 1  
1  
301  
Inception  
2025-08-15  
IMAX Chennai  
150  

Sample Output 1  
Movie show added successfully!  
ShowID: 301, Movie: Inception, Date: 2025-08-15, Theater: IMAX Chennai, Available Seats: 150 ShowID: 302, Movie: Interstellar, Date: 2025-08-20, Theater: PVR Mumbai, Available Seats: 200 (Here, Interstellar will appear first since it has more seats)  

Sample Input 2  
2  
301  
Inception  

Sample Output 2  
Seats updated successfully!  
ShowID: 301, Movie: Inception, Date: 2025-08-15, Theater: IMAX Chennai, Available Seats: 170 ShowID: 302, Movie: Interstellar, Date: 2025-08-20, Theater: PVR Mumbai, Available Seats: 200  

Sample Input 3  
3  
301  
Inception  

Sample Output 3  
Movie show deleted successfully!  
ShowID: 302, Movie: Interstellar, Date: 2025-08-20, Theater: PVR Mumbai, Available Seats: 200  

Sample Input 4  
4  

Sample Output 4  
ShowID: 302, Movie: Interstellar, Date: 2025-08-20, Theater: PVR Mumbai, Available Seats: 200  

Sample Input 5  
7  

Sample Output 5  
Invalid Choice  

## Notes:
- Use try, catch, and finally blocks to handle SQLException properly.  
- After every operation (insert, update, delete), display the list of shows sorted by available seats in descending order. Assume some records are already pre-populated.
