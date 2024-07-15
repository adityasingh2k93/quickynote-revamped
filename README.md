# Quicky Note

Quicky Note is a modern note-taking application designed to help users create, manage, and organize their notes efficiently. It offers features for adding, editing, pinning, and searching notes, along with user authentication and authorization.

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Running the Quicky Note Project](#running-the-quicky-note-project)
  - [Backend (Express.js)](#backend-expressjs)
  - [Frontend (React.js)](#frontend-reactjs)
- [Contributing](#contributing)
- [License](#license)

## Features

- **User Authentication**: Register and log in to manage your notes.
- **Note Management**: Create, edit, and delete notes.
- **Pin Notes**: Mark important notes to keep them at the top.
- **Search Notes**: Search for notes by title or content.
- **User-Specific Data**: Each user can manage their own notes.

## Tech Stack

- **Backend**: Node.js, Express.js
- **Frontend**: React.js
- **Database**: MongoDB Atlas
- **Authentication**: JSON Web Tokens (JWT), Bcrypt for password hashing

## Project Structure

```
/quicky-note
  ├── /backend
  │   ├── /models
  │   ├── /utilities
  │   ├── /config.json
  │   ├── /server.js
  │   ├── /package.json
  │   └── /...
  └── /frontend
      ├── /src
      ├── /public
      ├── /package.json
      └── /...
```

## Running the Quicky Note Project

### Backend (Express.js)

1. **Navigate to the `backend` folder in your terminal:**

   ```bash
   cd backend
   ```

2. **Run the following command to install the required dependencies:**

   ```bash
   npm install
   ```

3. **Connect to MongoDB Atlas:**

   - Go to [MongoDB Atlas](https://www.mongodb.com/).
   - Log in or create an account.
   - Create a new project by clicking the **“New Project”** button.
   - Enter the project name and click **“Next”**.
   - Add members if needed and click **“Create Project”**.
   - Click on the **“Database”** side menu and click **“Build a Database”**.
   - Select a free tier, name your cluster, select a server provider and region, and click **“Create Deployment”**.
   - In the **“Connect”** tab, choose **“Connect your application”** to access the Atlas database using Node.js.
   - Copy the connection string provided.
   - Paste the connection string into the `config.json` file:

     Before:
     ```json
     {
       "connectionString": "mongodb+srv://<username>:<password>@cluster0.mongodb.net/myFirstDatabase?retryWrites=true&w=majority"
     }
     ```

     After:
     ```json
     {
       "connectionString": "mongodb+srv://<username>:<password>@cluster0.mongodb.net/myFirstDatabase?retryWrites=true&w=majority"
     }
     ```

   - Replace `<password>` with the database user's password.

4. **Start the server:**

   ```bash
   npm start
   ```

### Frontend (React.js)

1. **Navigate to the `frontend` folder:**

   ```bash
   cd frontend/notes-app
   ```

2. **Run the following command to install the required dependencies:**

   ```bash
   npm install
   ```

3. **Start the React development server:**

   ```bash
   npm run dev
   ```

   This will start the frontend server and open the app in your default web browser.

## Contributing

At the moment, Quicky Note is not open for contributions.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

