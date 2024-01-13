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
- **Body:**
  - `username`: User's username
  - `password`: User's password
- **Description:** Handles user login. Requires username and password as parameters.

### 5. Register and Create User

- **Method:** POST
- **Path:** `/api/auth/create`
- **Body:**
  - `username`: New user's desired username
  - `password`: New user's password
- **Description:** Registers and creates a new user. Requires a unique username and a password for the new account.

### 6. Forget password
#### 6.1 Search user
- **Method:** POST
- **Path:** `/api/auth/forgetpassword/search`
- **Body:**
  - `username`: User's username
- **Description:** Searches for the user. If the user is found, proceeds to the next method.
#### 6.2 Change password
- **Method:** POST
- **Path:** `/api/auth/forgetpassword/change`
- **Body:**
  - `password`: New password for the user
- **Description:** Changes the user's password.

### 7. Change password
- **Method:** POST
- **Path:** `/api/auth/changepassword`
- **Body:**
  - `password`: Old password
  - `newPassword`: New password
- **Description:** Changes the user's password.

### 8. Delete user
- **Method:** DELETE
- **Path:** `/api/auth`
- **Description:** Delete the user's account.

### 9. Find user
#### 9.1 Find all
- **Method:** GET
- **Path:** `/api/user`
- **Description:** Find all users.
#### 9.2 Find One
- **Method:** GET
- **Path:** `/api/user/:id`
- **Parameter:**
  - `id`: id's user.
- **Description:** Find a user by ID.

### 10. Show friend
- **Method:** GET
- **Path:** `/api/user/friend`
- **Description:** Find friend's user.

### 11. Add friend
- **Method:** POST
- **Path:** `/api/user/friend/:id`
- **Parameter:**
  - `id`: Friend's ID.
- **Description:** Add friend method.

### 12. Delete friend
- **Method:** DELETE
- **Path:** `/api/user/friend/:id`
- **Parameter:**
  - `id`: a friend's id
- **Description:** Delete friend method.

### 13. Create Post
- **Method:** POST
- **Path:** `/api/post/`
- **Body:**
  - `title`: Title' post.
  - `description`: Description's post. no require.
  - `file`: File's post. no require.
- **Description:** Create a new post.

### 14. Like post
- **Method:** GET
- **Path:** `/api/post/like/:postId`
- **Paramerter:**
  - `postId`: Post's ID.
- **Description:** Like post.

### 15. Unlike post
- **Method:** GET
- **Path:** `/api/post/unlike/:postId`
  - `postId`: Post's ID.
- **Description:** Unlike post.

### 16. Find all post
- **Method:** GET
- **Path:** `/api/post`
- **Description:** Find all post.

### 17. Find one post
- **Method:** GET
- **Path:** `/api/post/:postId`
- **Parameter:**
  - `postId`: Post's ID.
- **Description:** Find one post.