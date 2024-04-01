# Expense Manager Application

## Problem Statement
The organization requires an Expense Manager Application to efficiently track employee income and expenses. As the number of employees grows, manual tracking becomes cumbersome and prone to errors. There is a need for a centralized system that can handle income and expenses seamlessly, providing insights for better financial management.

## Project Goal
The goal of this project is to develop a robust Expense Manager Application using modern web technologies. The application will allow users to input their income and expenses, categorizing them into various types for better organization and analysis. By leveraging Spring Boot, Hibernate, and MySQL, the application aims to provide a user-friendly interface for straightforward expense tracking through CRUD operations.

## Features of the Application
The Expense Manager Application will include the following features:

- **User Management**:
  - Create users to manage their income and expenses effectively.
  - Verify the existence of users within the system.

- **Income Management**:
  - Add income entries for each user.
  - View income details, including filtering options by day, month, and year.

- **Expense Management**:
  - Record expenses associated with each income entry.
  - Categorize expenses into various types for better analysis.

## Endpoints To Be Created
The following endpoints will be implemented to facilitate the functionality of the application:

### User Endpoints:
1. `GET "/users/allUsers"`:
   - Retrieves the list of all users from the database.
2. `GET "/users/{id}" (@PathVariable Integer id)`:
   - Fetches a user by the given Id.
3. `POST "/users/save" (@RequestBody User user)`:
   - Saves a new user into the database.
4. `POST "/users/checkUserExist" (@RequestBody User user)`:
   - Checks if the given user exists in the database.
5. `POST "/users/find" (@RequestBody User newUser)`:
   - Fetches the given user if found else returns null.
6. `GET "/users/filteredUserListByCalendar"`:
   - Fetches the list of all users by the given filters i.e., by Day, Month, and Year of IncomeDate.
7. `GET "/users/filteredUserListByType"`:
   - Fetches the list of all users by the given filter i.e., by IncomeType and ExpenseType.

### Income Endpoints:
1. `GET "/incomes/{incomeid}"`:
   - Retrieves the income for the given id.
2. `POST "/incomes/save/{userId}" (@PathVariable Integer userId, @RequestBody Income income)`:
   - Registers a new income for the given userId.

### Expense Endpoints:
1. `POST "/expenses/save/{incomeId}" (@PathVariable Integer incomeId, @RequestBody Expense expense)`:
   - Creates a new expense for a given incomeId.

These endpoints will form the backbone of the Expense Manager Application, providing essential functionality for users to manage their finances efficiently.
