# Three-Tier Web Application

A full-stack Task Management Web Application built using **React.js, Node.js, Express.js, and MongoDB**.

This application follows a three-tier architecture, separating the user interface, application logic, and database into independent layers.

## About the Project

The Three-Tier Task Manager is a simple web application designed to help users manage their daily tasks.

Users can create new tasks, view existing tasks, update their completion status, and delete tasks through an easy-to-use interface.

The application consists of three main components:

- **Frontend:** React.js provides the user interface.
- **Backend:** Node.js and Express.js handle application logic and REST API requests.
- **Database:** MongoDB stores and manages task information.

## Features

- Add new tasks.
- View all available tasks.
- Update task completion status.
- Delete existing tasks.
- REST API integration.
- Persistent task storage using MongoDB.
- Responsive and user-friendly interface.

## Technology Stack

| Component | Technology |
|---|---|
| Frontend | React.js |
| Programming Language | JavaScript |
| UI Library | Material UI |
| HTTP Client | Axios |
| Backend | Node.js |
| Backend Framework | Express.js |
| Database | MongoDB |
| Database ODM | Mongoose |

## Application Architecture

The application follows a three-tier architecture:

```text
             USER
               |
               v
       PRESENTATION LAYER
          React.js
               |
               | HTTP / REST API
               v
       APPLICATION LAYER
       Node.js + Express.js
               |
               | Mongoose
               v
          DATA LAYER
            MongoDB
               |
               v
          TASK DATA
```

### 1. Presentation Layer – Frontend

The frontend is developed using React.js.

It provides the interface through which users can interact with the task management application.

Axios is used to communicate with the backend REST APIs.

### 2. Application Layer – Backend

The backend is developed using Node.js and Express.js.

It handles incoming API requests and performs the required task management operations.

Mongoose is used to interact with the MongoDB database.

### 3. Data Layer – Database

MongoDB is used to store task information.

The backend communicates with MongoDB to create, retrieve, update, and delete task records.

## REST API Endpoints

| HTTP Method | Endpoint | Description |
|---|---|---|
| GET | `/api/tasks` | Retrieve all tasks |
| POST | `/api/tasks` | Create a new task |
| PUT | `/api/tasks/:id` | Update an existing task |
| DELETE | `/api/tasks/:id` | Delete a task |
| GET | `/ok` | Backend health-check endpoint |

## Project Structure

```text
Three-Tier-Web-Application/
│
├── Application-Code/
│   │
│   ├── frontend/
│   │   ├── public/
│   │   ├── src/
│   │   │   ├── services/
│   │   │   │   └── taskServices.js
│   │   │   ├── App.js
│   │   │   ├── App.css
│   │   │   ├── Tasks.js
│   │   │   ├── index.js
│   │   │   └── index.css
│   │   ├── Dockerfile
│   │   ├── package.json
│   │   └── package-lock.json
│   │
│   └── backend/
│       ├── models/
│       │   └── task.js
│       ├── routes/
│       │   └── tasks.js
│       ├── db.js
│       ├── index.js
│       ├── Dockerfile
│       ├── package.json
│       └── package-lock.json
│    
│
└── README.md
```

## Running the Application Locally

### Prerequisites

- Node.js
- npm
- MongoDB

### 1. Clone the Repository

```bash
git clone https://github.com/samir-shaikh7/Three-Tier-Web-Application.git

cd Three-Tier-Task-Manager
```

### 2. Start the Backend

```bash
cd Application-Code/backend

npm install
```

Configure the MongoDB connection:

```bash
export MONGO_CONN_STR="mongodb://localhost:27017/todo"
```

Start the backend:

```bash
node index.js
```

The backend runs on port `3500`.

### 3. Start the Frontend

Open another terminal:

```bash
cd Application-Code/frontend

npm install
```

Configure the backend API URL:

```bash
export REACT_APP_BACKEND_URL="http://localhost:3500/api/tasks"
```

Start the frontend:

```bash
npm start
```

The frontend runs on port `3000`.

## Author

**Samir Shaikh**

GitHub: https://github.com/samir-shaikh7