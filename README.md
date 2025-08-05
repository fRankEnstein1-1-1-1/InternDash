# InternDash

A simple internship dashboard prototype with a dummy login, user dashboard, and a backend API to serve user data. This project was created to fulfill the submission requirements for the SHECAN selection.

## Features

### Frontend
- **Dummy Login/Signup Page:** A basic login page that handles user signup and login without requiring actual authentication.
- **Dashboard:** Displays essential intern information, including a dummy name, referral code, and a total donations count fetched from the backend.
- **Rewards Section:** A static display of rewards and unlockables.

### Backend
- **REST API:** A RESTful API built with Node.js and Express that serves dummy data for user details and donations.
- **MongoDB Integration:** User data is stored in a MongoDB database (non-dynamic for this prototype).

- ## Setup and Installation

### Prerequisites
- Node.js (v18 or higher)
- npm (Node Package Manager)

### Backend Setup
1.  Navigate to the `backend` directory:
    ```bash
    cd backend
    ```
2.  Install dependencies:
    ```bash
    npm install
    ```
3.  Create a `.env` file with your MongoDB connection string:
    ```
    MONGO_URL="<your-mongodb-connection-string>"
    ```
4.  Start the backend server:
    ```bash
    node index.js
    ```
    (The server will run on port 5000)

### Frontend Setup
1.  Navigate to the `frontend` directory:
    ```bash
    cd frontend
    ```
2.  Install dependencies:
    ```bash
    npm install
    ```
3.  Create a `.env.local` file with the backend URL for local testing:
    ```
    REACT_APP_BACKEND_URL=http://localhost:5000
    ```
4.  Start the frontend application:
    ```bash
    npm start
    ```
    (The app will open in your browser on a port like 3000)

    ## API Endpoints

POST /sign
      ```json
      {
        "name": "string",
        "email": "string",
        "password": "string",
        "regid": "string"
      }
      ```
  POST /login
Description: Logs in a user and returns their data.
  Request Body:
      json
      {
        "email": "string"
      }
     
- POST /donation
    - Description: Adds to the user's donation total.
      Request Body:
      json
      {
        "email": "string",
        "donate": "number"
      }
     
