# README for the `mulesoft` Database

> [!NOTE]
> “[Syncing Customer Data Between Salesforce and a Relational Database: A Comprehensive Guide](https://mule.org.in/f/sync-customer-data-between-salesforce-db-a-comprehensive-guide)”
> [^2]:
> Dear readers,
> [^2]:
> In this comprehensive guide, we delve into the intricacies of synchronizing customer data between Salesforce and a relational database. Whether you’re a seasoned MuleSoft developer or just starting out, understanding this integration is crucial for efficient data management and seamless business processes.
> [^2]:
> Thanks in advance. 

> [!TIP]
> To stay updated on the latest news and insights on mule-related topics, follow us on:
> [^1]:
> [Subscribe for latest updates(✨🌟FREE✨🌟)](https://mule.org.in/m/create-account)
> [^1]:
> [Our website](https://mule.org.in/)
> [^1]:
> [Our WhatsApp channel](https://www.whatsapp.com/channel/0029VaIq2XrKbYMPKdl3YE3X)
> [^1]:
> [WhatsApp community](https://chat.whatsapp.com/F6cPb1xEsGdEJ7rrfEHN0H)
> [^1]:
> [Our LinkedIn page](https://www.linkedin.com/company/mule-trains/)

## Overview
The `mulesoft` database is designed to store customer information. It includes a single table called `Customer`, which holds details such as first names, last names, email addresses, and phone numbers.

## Table Structure
The `Customer` table has the following columns:

- `CustomerId`: An auto-incremented unique identifier for each customer.
- `FirstName`: Stores the first name of the customer.
- `LastName`: Stores the last name of the customer.
- `Email`: Serves as the primary key and stores the email address.
- `Phone`: Stores the customer's phone number.
- `CreatedDate`: Automatically set to the current timestamp when a record is inserted.
- `LastModifiedDate`: Automatically updated to the current timestamp when a record is modified.

## SQL Queries
Here are some common SQL queries you can use with the `Customer` table:

1. **Creating the `Database`:**
   
   ```sql
   CREATE DATABASE mulesoft;
   ```
      This query creates a new database named mulesoft.
  
2. **Using the mulesoft Database:**
   
   ```sql
   USE mulesoft;
   ```
      This command selects the mulesoft database for subsequent operations.
  
3. **Creating the `Customer` Table:**
   
   ```sql
   CREATE TABLE Customer (
    CustomerId INT AUTO_INCREMENT UNIQUE KEY,
    FirstName VARCHAR(255),
    LastName VARCHAR(255),
    Email VARCHAR(255),
    Phone VARCHAR(20),
    CreatedDate TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    LastModifiedDate TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    PRIMARY KEY (Email)
    );
   ```
      - `CustomerId`: An auto-incremented unique identifier for each customer.
      - `FirstName`: Stores the first name of the customer.
      - `LastName`: Stores the last name of the customer.
      - `Email`: Serves as the primary key and stores the email address.
      - `Phone`: Stores the customer's phone number.
      - `CreatedDate`: Automatically set to the current timestamp when a record is inserted.
      - `LastModifiedDate`: Automatically updated to the current timestamp when a record is modified.

4. **Inserting Data into the Customer Table:**
   
    ```sql
    INSERT INTO Customer (FirstName, LastName, Email, Phone)
    VALUES ('testuser', 'k', 'testuser-5@gmail.com', '9848022341');
    ```
    This query inserts a sample customer record into the Customer table.
  
5. **Updating a Record in the Customer Table:**
   
   ```sql
   UPDATE Customer
   SET LastName = 'test-3'
   WHERE Email = 'testuser-3@gmail.com';
   ```
     This query updates the last name of the customer with the email address ‘testuser-3@gmail.com’.
  
6. **Retrieving All Records from the Customer Table:**
   
   ```sql
   SELECT * FROM Customer;
   ```
     This query retrieves all records from the Customer table.

7. **Deleting All Records from the Customer Table:**
   
   ```sql
   DELETE FROM Customer;
   ```
     This query deletes all records from the Customer table.
   
9. **Dropping the Customer Table:**
    
   ```sql
   DROP TABLE Customer;
   ```
     This command removes the Customer table from the database.

