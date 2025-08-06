<img width="1315" height="693" alt="image" src="https://github.com/user-attachments/assets/76363362-5fae-4297-b96b-2b141df89a63" />


<img width="1365" height="701" alt="image" src="https://github.com/user-attachments/assets/3875d7f9-b511-453d-80c1-8ef470b2b2db" />




<img width="1342" height="700" alt="image" src="https://github.com/user-attachments/assets/a00b6600-ade7-4f59-8c5b-a7ac2c5cd0d3" />








Project Folder Structure
The project is organized into two main directories: backend for the Node.js API and frontend for the React application.
<img width="325" height="486" alt="image" src="https://github.com/user-attachments/assets/043b99cf-9e7b-45a4-8763-d471ac5d8dc0" /> 
                                                                                                                                                                           <img width="210" height="520" alt="image" src="https://github.com/user-attachments/assets/40366ae0-e3f6-43b4-afdb-bcab4cc4387b" />







My Full-Stack Task Tracker Application
This is a simple yet robust full-stack Task Tracker application designed to help users manage their daily tasks. It features a modern React frontend, a powerful Node.js Express backend, and a MySQL database for persistent data storage.

✨ Features
Add Tasks: Easily add new tasks with a title and an optional description.

View Tasks: Display all existing tasks in a clear, organized list.

Update Task Status: Mark tasks as complete or incomplete.

Delete Tasks: Remove tasks that are no longer needed.

Responsive Design: User-friendly interface that adapts to various screen sizes (mobile, tablet, desktop).

API-Driven: Frontend communicates with the backend via RESTful API endpoints.

Environment Variable Management: Secure handling of sensitive data (like database credentials) using .env files and platform-specific secret management.

🚀 Technologies Used
This application leverages the following technologies:

Frontend
React.js: A JavaScript library for building user interfaces.

Vite: A fast build tool for modern web projects.

Tailwind CSS: A utility-first CSS framework for rapid UI development.

Backend
Node.js: A JavaScript runtime environment.

Express.js: A fast, unopinionated, minimalist web framework for Node.js.

mysql2/promise: A MySQL client for Node.js with Promise-based API for asynchronous operations.

dotenv: A module to load environment variables from a .env file.

cors: Node.js middleware for providing a Connect/Express middleware that can be used to enable CORS with various options.

Database
MySQL: A popular open-source relational database management system.

Deployment Platforms
Frontend: Vercel (for static site hosting and continuous deployment from GitHub).

Backend: Render (for Node.js web service hosting).

Database: FreeSQLDatabase.com (for free MySQL hosting).

🛠️ Setup Instructions
To get this project running locally or understand its structure, follow these steps.

1. Database Setup (MySQL)
You've already set up your database using MySQL Workbench and FreeSQLDatabase.com. Ensure the following schema is applied to your freesqldatabase.com database:

Access phpMyAdmin: Log in to your freesqldatabase.com account and access phpMyAdmin.

Select your Database: Choose the database name provided by FreeSQLDatabase.com (e.g., sql5793125).

Execute SQL: Go to the "SQL" tab and run the following commands to create the tasks table:

USE sql5793125; -- Replace with your actual database name from FreeSQLDatabase.com

CREATE TABLE IF NOT EXISTS tasks (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    description TEXT,
    completed BOOLEAN DEFAULT FALSE,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Optional: Insert some dummy data
INSERT INTO tasks (title, description, completed) VALUES
('Learn Node.js', 'Understand Express and API creation.', FALSE),
('Setup MySQL', 'Create database and tables.', TRUE),
('Integrate Frontend', 'Connect React to Node.js API.', FALSE);

Note Credentials: Keep your DB_HOST (sql5.freesqldatabase.com), DB_USER, DB_PASSWORD, and DB_DATABASE (all from FreeSQLDatabase.com) handy.

2. Backend Setup (Node.js/Express)
Clone the Backend Repository:

git clone https://github.com/shegaw-21/Backend-Task-Tracker-App.git
cd Backend-Task-Tracker-App

Install Dependencies:

npm install

3. Frontend Setup (React/Vite)
Clone the Frontend Repository:

git clone https://github.com/shegaw-21/Frontend-Task-Tracker-App.git 

Install Dependencies:

npm install

Configure API Base URL:

For local development, y vite.config.js is already set up to proxy API requests to http://localhost:3001. No local .env file is strictly needed for the frontend for local proxying.

Run the Frontend Locally:

npm run dev

This will start the Vite development server, usually at http://localhost:5173/. Open this URL in your browser.

🚀 Deployment
The application is designed for deployment on cloud platforms for both frontend and backend.

Backend Deployment (Render)
Push Backend Code to GitHub: Ensure your Backend-Task-Tracker-App repository is pushed to GitHub.

Deploy to Render:

Sign up/log in to Render.

Create a new Web Service, connecting it to your backend GitHub repository.

Configure the service with Node runtime, npm install for build, and npm start for start command.

my database credentials as Environment Variables in Render's dashboard (DB_HOST, DB_USER, DB_PASSWORD, DB_DATABASE, PORT).

Deploy the service.

Copy the public URL provided by Render (e.g., https://your-backend-app.onrender.com). This is my Deployed Backend API URL.

Frontend Deployment (Vercel)
Push Frontend Code to GitHub: Ensure your Frontend-Task-Tracker-App repository is pushed to GitHub.

Deploy to Vercel:

Sign up/log in to Vercel.

Create a new Project, connecting it to my frontend GitHub repository.

Configure the project:

Root Directory: If your frontend is in a subfolder, specify it (e.g., frontend/).

Build Command: npm run build

Output Directory: dist (This is crucial, as Vite outputs to dist).

Add an Environment Variable in Vercel's dashboard:

Name: VITE_API_BASE_URL

Value: https://backend-task-tracker-app-9.onrender.com

Deploy the project.

Copy the public URL provided by Vercel (https://frontend-task-tracker-app-dmnm.vercel.app/). This is my Deployed Frontend App URL.


