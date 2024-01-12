# BASIC SOCIAL WEB API

- [Basic social web api](#basic-social-web-api)
  - [Path-and-services](#path-and-services)

## PATH AND SERVICES
  ### 1. Home

- **Method:** GET
- **Path:** `/`
- **Description:** Represents the home or main page of the API.

### 2. All API

- **Method:** GET
- **Path:** `/api`
- **Description:** Returns information about all available API endpoints.

### 3. Logout

- **Method:** GET
- **Path:** `/api/auth`
- **Description:** Represents the logout functionality.

### 4. Login

- **Method:** POST
- **Path:** `/api/auth`
- **Parameters:**
  - `username`: User's username
  - `password`: User's password
- **Description:** Handles user login. Requires username and password as parameters.

### 5. Register and Create User

- **Method:** POST
- **Path:** `/api/auth/create`
- **Parameters:**
  - `username`: New user's desired username
  - `password`: New user's password
- **Description:** Registers and creates a new user. Requires a unique username and a password for the new account.

### 6. Forget password
#### 6.1 Search user
- **Method:** POST
- **Path:** `/api/auth/forgetpassword/search`
- **Parameters:**
  - `username`: User's username
- **Description:** Searches for the user. If the user is found, proceeds to the next method.
#### 6.2 Change password
- **Method:** POST
- **Path:** `/api/auth/forgetpassword/change`
- **Parameters:**
  - `password`: New password for the user
- **Description:** Changes the user's password.

### 7. Change password
- **Method:** POST
- **Path:** `/api/auth/changepassword`
- **Parameters:**
  - `password`: Old password
  - `newPassword`: New password
- **Description:** Changes the user's password.

### 8. Delete user
- **Method:** DELETE
- **Path:** `/api/auth`
- **Description:** Delete the user's account.