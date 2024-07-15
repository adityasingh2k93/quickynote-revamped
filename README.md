# Quicky Note

Quicky Note is a modern note-taking application designed to help users create, manage, and organize their notes efficiently. It offers features for adding, editing, pinning, and searching notes, along with user authentication and authorization.

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Running the Quicky Note Project](#running-the-quicky-note-project)
  - [Backend (Express.js)](#backend-expressjs)
  - [Frontend (React.js)](#frontend-reactjs)
- [Feature Demo: Publishing Notes](#feature-demo-publishing-notes)
- [Contributing](#contributing)
- [License](#license)

## Features

- **User Authentication**: Register and log in to manage your notes.
- **Note Management**: Create, edit, and delete notes.
- **Pin Notes**: Mark important notes to keep them at the top.
- **Search Notes**: Search for notes by title or content.
- **User-Specific Data**: Each user can manage their own notes.
- **Publishing Notes** (Future Feature): Publish notes to your chosen platform with an API key and auth key.

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

## Feature Demo: Publishing Notes

We have a demo for a future feature that allows users to publish their notes to various platforms. Although this feature is not yet implemented in the current version of Quicky Note, you can self-host and experiment with it.

### How It Works

- **Publish Your Note**: In the future, users will be able to choose a platform from a dropdown menu (e.g., WordPress, Medium, etc.), enter their API key and authentication details, and publish the note directly to the selected platform.
- **Demo Available**: You can view a demo and self-host this feature by cloning the [feature branch](https://github.com/your-repo/quicky-note/tree/feature-publish-notes) from our GitHub repository.

### How to Self-Host the Publishing Notes Feature

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/your-repo/quicky-note.git
   cd quicky-note
   ```

2. **Checkout the Feature Branch:**

   ```bash
   git checkout feature-publish-notes
   ```

3. **Install Dependencies:**

   Follow the same instructions as in the [Running the Quicky Note Project](#running-the-quicky-note-project) section to install the dependencies for both the backend and frontend.

4. **Update Your Backend Code:**

   Add the necessary endpoints and functionality for publishing notes to different platforms as described in the [feature branch](https://github.com/your-repo/quicky-note/tree/feature-publish-notes).

5. **Run the Project:**

   Follow the [Backend](#backend-expressjs) and [Frontend](#frontend-reactjs) instructions to start the backend and frontend servers.

## Contributing

At the moment, Quicky Note is not open for contributions.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

