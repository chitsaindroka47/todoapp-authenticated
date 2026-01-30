# 📝 Todo Web App – Full Stack Application

A full-stack task management application built with **React.js, Node.js, Express, MongoDB Atlas, and Firebase Authentication**.  
Users can register, login, create boards, and manage todos with complete CRUD functionality.

---

## 🚀 Project Overview

Features:

- Firebase Email Authentication
- JWT based backend session
- Create multiple boards
- Add, update, delete todos
- Protected routes
- Clean UI

---
## Screenshots


## 🛠 Tech Stack

### Frontend
- React.js
- React Router DOM
- Firebase Authentication
- Axios

### Backend
- Node.js
- Express.js
- MongoDB Atlas + Mongoose
- Firebase Admin SDK
- JWT
- Express Validator
- CORS

---

## 📁 Project Structure

Humanli/
│
├── backend/
│ ├── config/
│ ├── controllers/
│ ├── middleware/
│ ├── models/
│ ├── routes/
│ ├── .env
│ ├── package.json
│ └── server.js
│
├── frontend/
│ ├── public/
│ ├── src/
│ │ ├── components/
│ │ ├── config/
│ │ ├── context/
│ │ ├── pages/
│ │ ├── services/
│ │ ├── App.js
│ │ └── index.js
│ ├── .env
│ └── package.json
│
└── README.md


---

## ⚙️ Setup Instructions

### Prerequisites
- Node.js (v16+ recommended)
- MongoDB Atlas Account
- Firebase Project
- npm

---

## 🔹 Backend Setup

```bash
cd backend
npm install
npm run dev
Backend runs on:

http://localhost:5000
🔹 Frontend Setup
cd frontend
npm install
npm start
Frontend runs on:

http://localhost:3000
🔐 Environment Variables
Backend (.env)
PORT=5000
NODE_ENV=development

MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/todoapp

FIREBASE_PROJECT_ID=xxxx
FIREBASE_PRIVATE_KEY_ID=xxxx
FIREBASE_PRIVATE_KEY="-----BEGIN PRIVATE KEY-----\nKEY\n-----END PRIVATE KEY-----\n"
FIREBASE_CLIENT_EMAIL=xxxx

JWT_SECRET=mysecretkey
JWT_EXPIRES_IN=7d

FRONTEND_URL=http://localhost:3000
Frontend (.env)
REACT_APP_FIREBASE_API_KEY=xxxx
REACT_APP_FIREBASE_AUTH_DOMAIN=xxxx.firebaseapp.com
REACT_APP_FIREBASE_PROJECT_ID=xxxx
REACT_APP_FIREBASE_STORAGE_BUCKET=xxxx.appspot.com
REACT_APP_FIREBASE_MESSAGING_SENDER_ID=xxxx
REACT_APP_FIREBASE_APP_ID=xxxx

REACT_APP_API_URL=http://localhost:5000/api/v1
🔑 Authentication Flow
User signs up / logs in using Firebase.

Firebase returns ID Token.

Frontend sends token in header:

Authorization: Bearer <firebase-id-token>
Backend verifies Firebase token.

Backend creates user (if new).

Backend returns JWT token.

Frontend stores JWT in localStorage.

All future API requests use:

Authorization: Bearer <jwt-token>
📡 API Endpoints
Base URL:

/api/v1
Auth
POST   /auth/register
GET    /auth/me
Boards
GET    /boards
POST   /boards
GET    /boards/:id
PUT    /boards/:id
DELETE /boards/:id
Todos
GET    /todos/boards/:boardId/todos
POST   /todos/boards/:boardId/todos
PUT    /todos/:id
DELETE /todos/:id
📦 Request Header Format
Authorization: Bearer <token>
Content-Type: application/json
🎯 Features
Email signup & login

JWT authentication

Board management

Todo CRUD

Protected routes

Priority based todos

🛡 Security
Firebase Authentication

JWT Authorization

Protected APIs

Environment variables

🧪 Test API
Open in browser:

http://localhost:5000/api/v1/auth/me
Should return:

No token provided
Means backend working.

👨‍💻 Author
Built by Chitranjan Singh
Frontend-focused Full Stack Developer