🏦 Banking Management System (Console-Based)
A robust, secure, and transaction-oriented Banking Management System built using Java and JDBC. This project demonstrates the implementation of core banking operations while ensuring data integrity and security through relational database management.

🌟 Key Features
User Authentication: Allows new users to register and existing users to securely log in using their email and password.

Account Creation: Users can open a new bank account linked to their profile with an automated unique account number generation system.

Transaction Management:

Credit Money: Add funds to the account instantly.

Debit Money: Withdraw funds with real-time balance validation.

Fund Transfer: Securely transfer money between two accounts using a dual-update logic (Debit from sender, Credit to receiver).

Security First: Every sensitive transaction (Debit, Credit, Transfer, Balance Check) requires a 4-digit Security Pin verification.

Data Integrity: Implemented ACID properties using JDBC commit() and rollback() to ensure transactions are either fully completed or not at all.

🛠️ Tech Stack
Language: Java (JDK 8 or higher)

Database: MySQL (Relational Database)

Driver: MySQL Connector/J (JDBC)

Development Environment: Visual Studio Code / IntelliJ IDEA

📊 Database Schema
The system relies on two primary tables in the banking_system database:

1. user Table
Stores the primary identity of the banking customers.
| Field | Type | Description |
| :--- | :--- | :--- |
| full_name | VARCHAR(255) | User's legal name |
| email | VARCHAR(255) (PK) | Unique identifier for login |
| password | VARCHAR(255) | Encrypted/Secure password |

2. accounts Table
Handles the financial data and account mapping.
| Field | Type | Description |
| :--- | :--- | :--- |
| account_number | BIGINT (PK) | Unique 8-digit account number |
| full_name | VARCHAR(255) | Account holder name |
| email | VARCHAR(255) (UNI) | Linked user email |
| balance | DECIMAL(10,2) | Current available balance |
| security_pin | CHAR(4) | Transaction authorization pin |

🚀 How to Run
Clone the Repository:

Bash
git clone https://github.com/princegupta9584/BankingManagementSystem.git
Database Setup:

Create a database named banking_system.

Use the schema provided in the image_ce0937.png to create user and accounts tables.

Update Credentials:

Open BankingApp.java and update the url, username, and password variables according to your local MySQL setup.

Compile & Run:

Bash
javac BankingManagementSystem/*.java
java BankingManagementSystem.BankingApp
