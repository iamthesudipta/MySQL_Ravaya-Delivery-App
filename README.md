# MySQL_Ravaya-Delivery-App
A small-scale online delivery app database designed for around 50 users, maintained by a college group. The database supports local community businesses by helping small business owners run their sales operations online with automated processes.

**MySQL Database Project :-**

**Scenario :**

Based in Kolkata, Saltlake Sector 1, "**Yours Store**" a small but modern market place which is since 1995. Now it is started online business based on Ravaya Super App. The store catagories the three product catagory - **Food**, **Household**, **Dailyneeds**. Every catagory have 10-15 items. To easy buy a smart team work a data analysis and share super savings discount based on items demand.

Now, Mr. Manoj Das the current owner aged 55 years old kin to learn technologies, his son also designed a python based simple app that integrate with dbms and payment, bookkeeping system.

**Prerequisites :**

You must first create the Little Lemon database in MySQL. You must also have the Customers, Bookings and Items tables created and populated with relevant data as shown below.

1. The code to create the database is as follows :

CREATE DATABASE IF NOT EXISTS Yours_Store;

2. The code to use the database is as follows :

use yours_store;

3. The code to create the Customers table is as follows 

CREATE TABLE customers (
CustomerID INT NOT NULL PRIMARY KEY,
FullName VARCHAR(100) NOT NULL,
PhoneNumber INT NOT NULL UNIQUE
);

4. The code to populate the Customers table is as follows
INSERT INTO Customers(CustomerID, FullName, PhoneNumber) VALUES
(1,"Sudipta Chatterjee", 0757536378),
(2,"Arezit Dutta",0757536329),
(3,"Somnath Sarkar",0757536372),
(4,"Debojoty Chatterjee",0757536371),
(5,"Urmila Thakur",0757536370),
(6,"Basab Roy",0757536375),
(7,"Mittir Masai",0757536365),
(8,"Feluda Feluda",0757536379);

The Customers table content is shown in the following screenshot :

![Image](https://github.com/user-attachments/assets/53fe954b-4d13-4228-96b0-905aeadecea7)

5. The code to create the Bookings table is as follows :

CREATE TABLE Bookings(
BookingID INT, Booking DATE,Quantity INT, CustomerID INT);

6. The code to populate the Bookings table with data is as follows :

INSERT INTO Bookings
(BookingID, Booking, Quantity, CustomerID)
VALUES
(10,"2024-10-1",15,1),
(11,"2024-10-2",35,2),
(12,"2024-10-3",45,3),
(13,"2024-10-4",55,4),
(14,"2024-10-5",95,5),
(15,"2024-10-6",105,6),
(16,"2024-10-7",205,7),
(17,"2024-10-8",310,8);

The Bookings table is shown in the following screenshot:

SELECT * FROM Bookings;

![image](https://github.com/user-attachments/assets/e9d9e57c-b999-4574-9d0d-9e85f10742f8)

7. The code to create the products is as follows :

CREATE TABLE Products(Products VARCHAR(255)PRIMARY KEY, Cost Decimal(4,2));

INSERT INTO Products(Products, Cost)
VALUES
("Biscut",25.50),
("Baby Food",45.95),
("Sweet",95.25),
("Rice",75.10),
("Meat",82.50);

The Products table is shown in the following screenshot :

![image](https://github.com/user-attachments/assets/9fc3903b-b5ab-4ab5-8335-fb17a85d1be5)


Task Instructions :

Task 1: Filter data using the WHERE Clause and Logical Operators.

Create SQL statement to print all records from Bookings table for the following bookings dates using the BETWEEN operator: 2024-10-3, 2021-10-6 and 2024-10-8.

The expected output result should be the same as shown in the following screenshot :

**SELECT *
FROM Bookings
WHERE Booking between "2024-10-3" and "2024-10-8";**

![image](https://github.com/user-attachments/assets/f5682cf4-c72c-43f0-aed7-8a39b54a309d)


Task 2: Create a JOIN Query.

Create a JOIN SQL statement on the Customers and Bookings tables. The statement must print the customers full names and related bookings IDs from the date 2024-04-05.

**SELECT *
FROM Customers
INNER JOIN Bookings ON Customers.CustomerID=Bookings.CustomerID;**


![image](https://github.com/user-attachments/assets/fdb6972a-5a5a-47d9-ad4b-df15a022cc21)

Task 3: Create a REPLACE Statement.

Create a SQL REPLACE statement that updates the cost of the Sweet from $95.25 to $20.25. The expected output result should be the same as that shown in the following screenshot :
**
**REPLACE INTO Products (Products,Cost) VALUES ("Sweet",20.25);**
**
**SELECT *
FROM Products;**

![image](https://github.com/user-attachments/assets/a17b7cf9-8cd3-448a-a5fb-c996bb303f3e)

Task 4: Create Constraints.

Create a new table called "DeliveryAddress" in the Yours_Store database with the following columns and constraints :
ID: INT PRIMARY KEY

Address: VARCHAR(255) NOT NULL

Type: NOT NULL DEFAULT "Private"

CustomerID: INT NOT NULL FOREIGN KEY referencing CustomerID in the Customers table

**CREATE TABLE DeliveryAddress (
ID INT NOT NULL PRIMARY KEY,
Address VARCHAR(255) NOT NULL,
Type VARCHAR(100) NOT NULL DEFAULT"Private",
CustomerID INT NOT NULL, 
FOREIGN KEY(CustomerID) References Customers(CustomerID)
);**


![image](https://github.com/user-attachments/assets/f0ccbcbc-9037-4efa-b2a0-21a2266ce66a)

![image](https://github.com/user-attachments/assets/268962f5-52ce-4647-9df7-ea491eb80106)

Task 5: Alter Table Structure.

Create a SQL statement that adds a new column called '**Products**' to the Courses table.

GroupProducts: VARCHAR(255)

**ALTER TABLE Products
ADD  GroupProducts VARCHAR(255);**


![image](https://github.com/user-attachments/assets/8fde53ac-e6c7-4ee3-aab4-2470bd8293f9)

Task 6: Create a Subquery.

Create a SQL statement with a subquery that prints the full names of all customers who made bookings on the following date: 2024-10-5.

**SELECT *
FROM customers 
WHERE CustomerID=(Select CustomerID FROM Bookings WHERE Booking = "2024-10-5");**


![image](https://github.com/user-attachments/assets/ee55359a-ba56-4b68-a34e-ec50307abf00)














