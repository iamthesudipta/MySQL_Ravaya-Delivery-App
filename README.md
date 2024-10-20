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

