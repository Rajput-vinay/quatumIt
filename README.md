# QuantumIt Assignment

## Project Overview
This project is a **Login and Registration System** built using **React.js** for the frontend and **Node.js** with **MongoDB** for the backend. The system allows users to register, log in, and view a protected static table with user information.

## Tech Stack
- Frontend: React.js
- Backend: Node.js, Express.js
- Database: MongoDB
- Authentication: JSON Web Token (JWT)
- Storage: LocalStorage

## Features
- User Registration
- User Login
- Protected Route (User Dashboard)
- JWT Authentication
- LocalStorage for user session management
- Responsive Design

## Folder Structure
```
📁 Backend
├─ models/               
├─ routes/     
├─ controller/               
├─ database/           
└─ index.js             

📁 Frontend
├─ src/
│  ├─ component/        
│  ├─ pages/             
│  ├─ App.js             
│  └─ index.js           
└─ package.json          
```

## Project Overview
 - Signup page
  https://github.com/Rajput-vinay/quatumIt/blob/main/frontend/src/assets/signuppage.jpg?raw=true

 -Sigin Page
 https://github.com/Rajput-vinay/quatumIt/blob/main/frontend/src/assets/sigin.jpg?raw=true 

 - user page
 https://github.com/Rajput-vinay/quatumIt/blob/main/frontend/src/assets/user.jpg?raw=true
## Installation
### Prerequisites
- Node.js
- MongoDB

### Backend Setup
1. Navigate to the backend folder:
   ```bash
   cd backend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file and add your MongoDB URI and JWT Secret:
   ```env
   PORT = your_port
   MONGODB_URI=your_mongodb_uri
   JWT_SECRET=your_jwt_secret
   ```
4. Start the backend server:
   ```bash
   npm start
   ```

### Frontend Setup
1. Navigate to the frontend folder:
   ```bash
   cd frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the React application:
   ```bash
   npm start
   ```

## API Endpoints
### 1. User Registration
**POST** `/api/v1/signup`
#### Request Body:
```json
{
  "name": "John Doe",
  "dob": "05-12-1998",
  "email": "johndoe@example.com",
  "password": "password123"
}
```
#### Response:
```json
{
  "message": "Successful Register",
  
}
```

### 2. User Login
**POST** `/api/v1/signin`
#### Request Body:
```json
{
  "email": "johndoe@example.com",
  "password": "password123"
}
```
#### Response:
```json
{
  "token": "jwt_token",
  
}
```

## Protected Route
- After login or registration, the user is redirected to a protected dashboard page.
- The JWT token and user information are saved in **LocalStorage**.
- The dashboard displays a static table with sample data.
- If the user is not logged in, they cannot access the dashboard.

## Environment Variables
| Key         | Description       |
|-------------|------------------|
| MONGO_URI   | MongoDB Connection URI |
| JWT_SECRET  | JWT Secret Key |

## How to Run
1. Start MongoDB service.
2. Run backend and frontend servers.
3. Open the app at: `http://localhost:3000`

## Author
**Vinay Rajput**

## License
This project is licensed under the MIT License.

