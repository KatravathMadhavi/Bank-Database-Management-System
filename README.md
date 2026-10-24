# Bank Database Management System

## About the Project

We developed this Bank Database Management System as a team project to understand how banking operations can be managed using a full-stack web application.

The application provides separate functionalities for customers and administrators. Customers can register, log in, request bank accounts, perform banking transactions, view their transaction history, and apply for loans. Administrators can manage customer accounts, review loan applications, and handle different banking operations.

The main objective of our project was to build a database-driven application that demonstrates basic banking workflows while helping us gain practical experience in frontend development, backend development, database management, and API integration.

## Features

### Customer Features

* **User Registration and Login:** Customers can register and log in to access the application.
* **Account Management:** Customers can request bank accounts and view their account information.
* **Deposits and Withdrawals:** Supports deposit and withdrawal operations.
* **Fund Transfers:** Supports transferring funds between accounts.
* **Transaction History:** Maintains records of transactions performed through the application.
* **Loan Applications:** Customers can apply for different types of loans.
* **EMI Payments:** Includes functionality for loan EMI payments.

### Admin Features

* **Account Management:** Administrators can review account requests and manage account statuses.
* **Loan Management:** Administrators can review loan applications and perform supported approval, rejection, and disbursement operations.
* **Dashboard:** Provides access to administrative statistics and banking-related information.
* **Banking Operations:** Supports administrative management of relevant account and loan workflows.

## Technologies Used

### Frontend

* React.js
* Vite
* React Router
* Axios
* CSS

### Backend

* Node.js
* Express.js
* Sequelize ORM
* JSON Web Token (JWT)
* bcryptjs
* dotenv

### Database

* MySQL

## Project Modules

### 1. User Authentication

The authentication module handles customer registration and login. Passwords are hashed using bcryptjs, and JWT is used to authenticate requests to protected backend routes.

The application also distinguishes between customer and administrator roles to provide access to the appropriate functionalities.

### 2. Account Management

This module manages account requests and account information. The application supports different account types, including savings and current accounts.

Accounts can have different statuses depending on their stage in the account management process. Administrators can review account requests and manage account statuses.

### 3. Transaction Management

The transaction module handles operations such as deposits, withdrawals, and fund transfers.

Transaction records include information such as transaction type, amount, account details, and the balance after the transaction. Database transactions are used in relevant operations to help maintain consistency when multiple related database changes are required.

### 4. Loan Management

The loan module allows customers to submit loan applications and retrieve their loan information.

The application supports different loan categories, including:

* Home loans
* Car loans
* Personal loans
* Education loans
* Business loans

Administrators can manage loan applications through the supported approval and rejection workflows. The backend also includes functionality for loan disbursement and EMI payments.

### 5. Admin Dashboard

The admin module provides functionalities for managing customer accounts and loan applications. It also includes routes for retrieving administrative statistics and other banking-related information.

## Database Design

We used MySQL to store and manage the application's data. Sequelize ORM connects the backend to the database and provides a structured way to perform database operations.

The application includes the following main database models:

* **User:** Stores user information, authentication details, and roles.
* **Account:** Stores account numbers, account types, balances, interest rates, and account statuses.
* **Transaction:** Stores transaction types, amounts, account details, and related transaction information.
* **Loan:** Stores loan types, amounts, interest rates, EMI-related information, and loan statuses.

These models represent the main entities involved in the application's banking workflows.

## How the Application Works

The frontend is developed using React, while the backend uses Node.js and Express.js to handle requests and application logic.

The frontend communicates with the backend through REST APIs. When a user performs an operation, such as requesting an account or viewing transaction details, the frontend sends a request to the appropriate backend endpoint.

The backend processes the request, interacts with the MySQL database through Sequelize, and returns a response to the frontend.

JWT authentication is used for protected requests, while role-based authorization helps separate customer and administrator functionalities.



## Testing

The application can be checked manually by testing the main workflows:

1. Register a customer account and log in.
2. Test account requests and account management.
3. Test deposit and withdrawal operations using test data.
4. Test fund transfers and transaction history.
5. Submit a loan application.
6. Check the relevant administrator workflows.

These are suggested testing steps; not all workflows have been independently verified.

The frontend includes linting and production-build scripts. To run them, navigate to the frontend directory and execute:

```bash
npm run lint
npm run build
```

Automated backend tests can be added to improve reliability and verify the application's API endpoints.

## What We Learned

Through this project, our team gained practical experience in:

* Building a full-stack web application using React and Node.js.
* Developing REST APIs using Express.js.
* Connecting a backend application to MySQL using Sequelize ORM.
* Implementing authentication using JWT.
* Hashing passwords using bcryptjs.
* Designing database models for users, accounts, transactions, and loans.
* Integrating frontend components with backend APIs.
* Understanding how database transactions help maintain consistency during related operations.
* Implementing different workflows for customers and administrators.

## Future Improvements

Some improvements that could be made to the project include:

* Adding automated unit and integration tests.
* Improving input validation and error handling.
* Adding transaction filtering and detailed reports.
* Improving the user interface and mobile responsiveness.
* Strengthening authorization and administrative security.
* Adding audit logs for sensitive banking operations.
* Improving database migrations and schema management.
* Documenting API endpoints with example requests and responses.

## Conclusion

Working on this project helped our team understand how the frontend, backend, and database work together to build a full-stack application.

It gave us practical experience with web development, database design, API integration, authentication, and the implementation of basic banking workflows. The project also helped us understand the importance of data consistency and access control when developing applications that manage sensitive information.

## Disclaimer

This project was developed by our team for educational purposes only. It is a demonstration of basic banking operations and is not intended for production banking, real financial transactions, or the storage of actual customer banking information.
