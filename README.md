User-Authentication-API-with-Express-and-SQLite


This is a simple and secure **User Authentication API** built using **Node.js**, **Express**, **SQLite**, and **bcrypt** for password hashing. The API supports basic user authentication functionality, including **registration**, **login**, and **password change**.

The application uses **SQLite** as the database to store user data and **bcrypt** to securely hash and compare passwords. This project demonstrates a simple approach to managing user credentials while implementing essential security practices.

## Features:
- **User Registration**: Create a new user account with a unique username and strong password.
- **User Login**: Authenticate users with their username and password.
- **Password Change**: Allow users to update their password with additional security checks.
- **Password Hashing**: Passwords are hashed using **bcrypt** to ensure secure storage.

## Endpoints:
- **POST /register**: Register a new user.
  - Request body: `{ username, name, password, gender, location }`
  - Response: Success or error message.

- **POST /login**: Login with an existing user.
  - Request body: `{ username, password }`
  - Response: Success or error message.

- **PUT /change-password**: Change the current user's password.
  - Request body: `{ username, oldPassword, newPassword }`
  - Response: Success or error message.

## Setup and Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/user-auth-api.git
   cd user-auth-api
