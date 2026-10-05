# 📚 Node_React_CRUD

A robust Node.js application designed to efficiently test for various Purpose. Utilizing Express for the backend, MySQL for database management, and React for the frontend interface, this system facilitates CRUD operations with seamless CORS handling and environment variable management.

## Tech Stack

**Client:** React, Bootstrap

**Server:** Node, Express

**Database:** MYSQL

## 📦 Installation

Before installing check Nodejs  `preferred Node Version v22.2.0`  on your system, MYSQL Database (if using local)

```bash
    git clone https://github.com/soocrates/Node_React_CRUD.git 
    cd Node_React_CRUD
```

**File Structure:**  After cloning you see `frontend` and `backend` directory and overall project will look like this

```
    soocrates@ubuntu:~/Node_React_CRUD $ tree -L 2
    ├── backend
    │   ├── connection.js
    |   ├── .env.sample
    │   ├── index.js
    │   ├── package.json
    │   ├── package-lock.json
    │   └── secret_manager.js
    ├── db.sql
    ├── frontend
    │   ├── dist
    │   ├── index.html
    │   ├── package.json
    │   ├── package-lock.json
    │   ├── public
    │   ├── src
    │   └── vite.config.js
    └── README.md
```

## 🔧 Environment Variables

Create a `.env` file inside `backend` directory of your project from `.env.sample`:

```
APP_PORT=3000  

### DB_HOST could be remote host, proxy or localhost URL but must me mysql
DB_HOST= env-example-db.cfasdfasr34dsadc4.us-east-1.rds.amazonaws.com
DB_PORT=3306
DB_NAME=test_db

### From where you want use Credentials
#   Options Could be  
#   1. from_secret  (to pass creds from aws secret)
### 2. from_env  (to pass creds from env)

CRED= from_secret

### If you are Passing Credentials Directly from ENV
DB_USER= test_user
DB_PASSWORD= test_0000

### If you are using AWS Secret Manager 
AWS_REGION = us-east-1
AWS_SECRET_NAME = test-secret-manager
```

## 🚀 Running the Application

### Start the Backend Server

```bash
    cd Node_React_CRUD 
    cd backend
    npm install
    node app.js
```

### Start the Frontend Development Server

```bash
    cd Node_React_CRUD 
    cd frontend
    npm install
    npm start
```

## 🌐 Backend Endpoints

### Fetch All Students

* **URL:** `/students`
* **Method:** `GET`
* **Response:** JSON array of student records

### Fetch a Student by ID

* **URL:** `/student/:id`
* **Method:** `GET`
* **Response:** JSON object of the student record

### Create a Student Record

* **URL:** `/create`
* **Method:** `POST`
* **Request Body:**
```
  {
      "name":"Student Name",
      "dob":"YYYY-MM-DD",
      "result":"Pass/Fail"
  }
```
* **Response:** Success or error message

### Update a Student Record
* **URL:** `/update/:id`
* **Method:** `PUT`
* **Request Body:**
```
  {
      "name":"Updated Student Name",
      "dob":"YYYY-MM-DD",
      "result":"Pass/Fail"
  }
```
* **Response:** Success or error message

### Delete a Student Record

* **URL:** `/delete/:id`
* **Method:** `DELETE`
* **Response:** Success or error message

## 📚 Dependencies

### Backend

* `express`: Web framework for Node.js
* `mysql`: MySQL client for Node.js
* `cors`: Middleware for handling Cross-Origin Resource Sharing
* `dotenv`: Module to load environment variables from a `.env` file

### Frontend

* `react`: JavaScript library for building user interfaces
* `axios`: Promise-based HTTP client for the browser and Node.js
* `react-router-dom`: DOM bindings for React Router

## DevOps



## 🛠️ Contributing

Contributions are welcome Please feel free to submit a pull request or open an issue if you encounter any problems.
Thank you #