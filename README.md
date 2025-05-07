# Clinic Booking System Database

## Description  
This project is a relational database designed for managing a clinic's operations, including:  
- **Department and doctor management**  
- **Patient registration and appointments**  
- **Medical record tracking**  
- **Scheduling with conflict prevention**  

Built using MySQL, it ensures data integrity with constraints, foreign keys, and unique indexes.  

## Setup Instructions  

### Prerequisites  
- MySQL Server installed (e.g., MySQL 8.0+)  
- A database client (e.g., MySQL Workbench, phpMyAdmin)  

### Import the SQL File  
1. Create a new database:  
   ```sql
   CREATE DATABASE clinic_db;
   USE clinic_db;
   Import the provided db.sql file:
2.bash
mysql -u [username] -p clinic_db < path/to/db.sql
MySQL Workbench:
Use the Data Import/Restore tool and select db.sql.

![ERD](/asset\ER Diagram.drawio.svg)






