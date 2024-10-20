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









