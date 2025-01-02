# Squid Quiz

## Table of Contents

1. [Introduction](#introduction)
2. [Project Structure](#project-structure)
3. [Setup Instructions](#setup-instructions)
4. [Running the Project](#running-the-project)
5. [File Descriptions](#file-descriptions)
   - [Root Files](#root-files)
   - [Waste Folder](#waste-folder)
   - [Config Folder](#config-folder)
   - [Src Folder](#src-folder)
6. [API Endpoints](#api-endpoints)
7. [Technologies Used](#technologies-used)

---

## Introduction

Squid Quiz is a Node.js-based project with multiple features, including user authentication, email integration, and database interactions. This documentation provides a complete overview of the project structure and guidance for setup, execution, and development.

---

## Project Structure

```
Squid_Quiz-main
├── .gitignore
├── index.js
├── package-lock.json
├── package.json
├── server.js
├── Waste/
├── config/
├── src/
```

### Key Directories

- **Waste**: Contains unused or experimental scripts.
- **Config**: Configuration files for MongoDB, Nodemailer, and Passport.
- **Src**: Core project files, including controllers, middleware, models, and routes.

---

## Setup Instructions

1. **Clone the Repository:**

   ```bash
   git clone <repository-url>
   cd Squid_Quiz-main
   ```

2. **Install Dependencies:**

   ```bash
   npm install
   ```

3. **Configure Environment Variables:**
   Create a `.env` file in the root directory with the following variables:

   ```env
   MONGO_URI=<MongoDB connection string>
   EMAIL_USER=<Email address>
   EMAIL_PASS=<Email password>
   JWT_SECRET=<JWT secret key>
   ```

4. **Setup Database:**
   Ensure MongoDB is running and accessible with the connection string in `MONGO_URI`.

---

## Running the Project

1. **Start the Development Server:**

   ```bash
   npm start
   ```

   The app will run at [http://localhost:3000](http://localhost:3000).

2. **Production Build:**

   ```bash
   npm run build
   ```

3. **Run Tests:**

   ```bash
   npm test
   ```

---

## File Descriptions

### Root Files

- **`.gitignore`**: Specifies files and directories to ignore in version control.
- **`index.js`**: Entry point of the application.
- **`package.json`**: Contains project metadata and dependencies.
- **`server.js`**: Main server file that initializes the application.

### Waste Folder

Contains experimental or deprecated scripts:

- **`Final.js`**: Placeholder script.
- **`checkToken.js`**: Token validation logic (deprecated).
- **`firstlogin.js`**: Handles user first login scenarios (deprecated).
- **`isSelected.js`**: Logic for selection tracking.
- **`s1.js`**: Miscellaneous script.
- **`saveToken.js`**: Saves tokens to storage (deprecated).
- **`thank.js`**: Generates a thank-you message (deprecated).

### Config Folder

Configuration files:

- **`mongo.config.js`**: MongoDB connection setup.
- **`nodemailer.config.js`**: Email setup using Nodemailer.
- **`passport.config.js`**: Authentication strategies using Passport.js.

### Src Folder

#### Controller

- **`controller.js`**: Handles core application logic.
- **`loginController.js`**: Manages user login and authentication.

#### Middleware

- **`checkaccess.js`**: Middleware to check user permissions.
- **`confirm.js`**: Middleware for user confirmation flows.

#### Model

- **`LoginSchema.js`**: Mongoose schema for user login.
- **`Squid.js`**: Core model for the application.
- **`user.repo.js`**: Repository for user-related database operations.

#### Routes

- **`user_routes.js`**: Defines API endpoints for user-related operations.

---

## API Endpoints

### User Routes

- **`POST /login`**: User login.
- **`POST /register`**: User registration.
- **`GET /profile`**: Fetch user profile.
- **`PUT /update`**: Update user details.

### Admin Routes

- **`GET /admin/users`**: Fetch all users (admin only).
- **`DELETE /admin/user/:id`**: Delete a user by ID (admin only).

---

## Technologies Used

- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: Passport.js, JWT
- **Email Service**: Nodemailer
- **Other Tools**: Mongoose, Bcrypt.js

---

For further assistance or to contribute to the project, please refer to the contribution guidelines or contact the project maintainers.

