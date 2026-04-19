 🌍 Travel Booking System

A simple **Travel Booking System** developed using **Python and MySQL**.
This project allows users to manage customers, travel packages, and bookings through a menu-driven interface.

 📌 Features

* ➕ Add Customer Details
* 🧳 Add Travel Packages
* 📅 Book Trips
* 📋 View All Bookings
* 🔗 Uses relational database (MySQL)

 🛠️ Technologies Used

* Python
* MySQL
* mysql-connector-python
* VS Code


 🗄️ Database Structure

1. Customers Table

* `customer_id` (Primary Key)
* `name`
* `email`
2. Packages Table

* `package_id` (Primary Key)
* `destination`
* `price`

 3. Bookings Table

* `booking_id` (Primary Key)
* `customer_id` (Foreign Key)
* `package_id` (Foreign Key)
* `travel_date`


 ⚙️ Setup Instructions
 Step 1: Install Dependencies

bash
pip install mysql-connector-python
Step 2: Setup MySQL Database

Run the following SQL:

sql
CREATE DATABASE travel_system;
USE travel_system;

CREATE TABLE Customers (
    customer_id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100)
);

CREATE TABLE Packages (
    package_id INT AUTO_INCREMENT PRIMARY KEY,
    destination VARCHAR(100),
    price INT
);

CREATE TABLE Bookings (
    booking_id INT AUTO_INCREMENT PRIMARY KEY,
    customer_id INT,
    package_id INT,
    travel_date DATE,
    FOREIGN KEY (customer_id) REFERENCES Customers(customer_id),
    FOREIGN KEY (package_id) REFERENCES Packages(package_id)
);
 Step 3: Run the Program
`bash
python travel_system.py


 🧪 How to Use

1. Add Customer
2. Add Package
3. Book Trip
4. View Bookings

 📷 Output

(Console-based output showing customer bookings)

 🚀 Future Improvements

* Add GUI using Tkinter
* Add Update/Delete features
* Add user authentication
* Convert into web application

 👩‍💻 Author

Jasmine
