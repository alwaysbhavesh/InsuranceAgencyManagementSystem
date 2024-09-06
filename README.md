# Insurance Agency Management System

## Overview

The Insurance Agency Management System is a Java console application designed for managing insurance policies, clients, and claims. This application showcases the use of Core Java, MySQL, and JDBC through a menu-driven interface, enabling users to perform various CRUD operations.

## Features

### Policy Management
- **Add a New Policy**: Create and store new policy details.
- **View Policy Details**: Retrieve and display policy information.
- **Update Policy Information**: Modify existing policy details.
- **Delete a Policy**: Remove a policy from the system.

### Client Management
- **Register a New Client**: Add new client information to the system.
- **View Client Details**: Access and view client details.
- **Update Client Information**: Update existing client data.
- **Delete a Client**: Remove a client from the system.

### Claim Management
- **Submit a New Claim**: Create and store new claim details.
- **View Claim Details**: Retrieve and display claim information.
- **Update Claim Information**: Modify existing claim details.
- **Delete a Claim**: Remove a claim from the system.

## Database Schema

Ensure the following tables exist in your database:

### `Policy` Table
- **Columns**:
    - `policy_id` (Primary Key)
    - `policy_number`
    - `type`
    - `coverage_amount`
    - `premium_amount`

### `Client` Table
- **Columns**:
    - `client_id` (Primary Key)
    - `name`
    - `email`
    - `phone_number`
    - `address`

### `Claim` Table
- **Columns**:
    - `claim_id` (Primary Key)
    - `policy_id` (Foreign Key referencing Policy Table)
    - `client_id` (Foreign Key referencing Client Table)
    - `claim_date`
    - `status` (e.g., submitted, processed)

## Prerequisites

- Java Development Kit (JDK) 11 or higher
- MySQL or a compatible SQL database
- Database schema with `Policy`, `Client`, and `Claim` tables

## Setup

### Database Configuration
1. Update the `DatabaseConnection` class in the `com.cts.insurancemanagement.util` package with your database credentials.

### Compile and Run
1. Compile the Java files:
    ```bash
    javac -d bin src/com/cts/insurancemanagement/*.java
    ```
2. Run the application:
    ```bash
    java -cp bin com.cts.insurancemanagement.Main
    ```

## Usage

### Menu Options
1. **Policy Management**
    - Add New Policy
    - View Policy Details
    - Update Policy Information
    - Delete Policy

2. **Client Management**
    - Register New Client
    - View Client Details
    - Update Client Information
    - Delete Client

3. **Claim Management**
    - Submit New Claim
    - View Claim Details
    - Update Claim Information
    - Delete Claim

## Implimented

- Developed a menu-based console application using Core Java.
- Used JDBC for database interactions.
- Implemented menu options for managing policies, clients, and claims.
- Ensured that claim statuses are updated appropriately.
- Handled exceptions effectively and provide user-friendly error messages.
- Also ensured clean, well-documented code adhering to standard coding conventions.

## License

This project is licensed under the MIT License.

---
