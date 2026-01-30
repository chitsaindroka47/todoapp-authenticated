# 📝 Todo Web App – Full Stack Application

A full-stack task management application built using **React.js, Node.js, Express.js, MongoDB Atlas, and Firebase Authentication**.  
Users can sign up, log in, create boards, and manage todos with complete CRUD functionality.

---

## 🚀 Project Overview

This application provides:

- Firebase Email Authentication  
- JWT based backend authentication  
- Board management  
- Todo management  
- Protected routes  
- Clean and simple UI  

---

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
- JSON Web Token (JWT)  
- Express Validator  
- CORS  

---

## 📁 Project Structure

```
Humanli/
│
├── backend/
│   ├── config/
│   │   ├── database.js
│   │   └── firebase.js
│   ├── controllers/
│   │   ├── authController.js
│   │   ├── boardController.js
│   │   └── todoController.js
│   ├── middleware/
│   │   ├── auth.js
│   │   └── errorHandler.js
│   ├── models/
│   │   ├── User.js
│   │   ├── Board.js
│   │   └── Todo.js
│   ├── routes/
│   │   ├── authRoutes.js
│   │   ├── boardRoutes.js
│   │   └── todoRoutes.js
│   ├── .env
│   ├── package.json
│   └── server.js
│
├── frontend/
│   ├── public/
│   │   └── index.html
│   ├── src/
│   │   ├── components/
│   │   │   └── ProtectedRoute.js
│   │   ├── config/
│   │   │   └── firebase.js
│   │   ├── context/
│   │   │   └── AuthContext.js
│   │   ├── pages/
│   │   │   ├── Login.js
│   │   │   ├── Signup.js
│   │   │   ├── Dashboard.js
│   │   │   └── BoardDetail.js
│   │   ├── services/
│   │   │   └── api.js
│   │   ├── App.js
│   │   └── index.js
│   ├── .env
│   └── package.json
│
└── README.md
```

---

## ⚙️ Setup Instructions

### Backend Setup

```bash
cd backend
npm install
npm run dev
```

Backend runs on:

```
http://localhost:5000
```

---

### Frontend Setup

```bash
cd frontend
npm install
npm start
```

Frontend runs on:

```
http://localhost:3000
```

---

## 🔐 Environment Variables

### Backend (.env)

```env
PORT=5000
NODE_ENV=development

MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/todoapp

FIREBASE_PROJECT_ID=your_project_id
FIREBASE_PRIVATE_KEY_ID=your_key_id
FIREBASE_PRIVATE_KEY="-----BEGIN PRIVATE KEY-----\nKEY\n-----END PRIVATE KEY-----\n"
FIREBASE_CLIENT_EMAIL=your_service_account_email

JWT_SECRET=mysecretkey
JWT_EXPIRES_IN=7d

FRONTEND_URL=http://localhost:3000
```

---

### Frontend (.env)

```env
REACT_APP_FIREBASE_API_KEY=your_key
REACT_APP_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
REACT_APP_FIREBASE_PROJECT_ID=your_project_id
REACT_APP_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
REACT_APP_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
REACT_APP_FIREBASE_APP_ID=your_app_id

REACT_APP_API_URL=http://localhost:5000/api/v1
```

---

## 🔑 Authentication Flow

1. Firebase login/signup  
2. Firebase returns ID Token  
3. Frontend sends token in header  
4. Backend verifies token  
5. Backend returns JWT  
6. JWT stored in localStorage  

---

## 📡 API Endpoints

### Auth
```
POST /auth/register
GET  /auth/me
```

### Boards
```
GET    /boards
POST   /boards
PUT    /boards/:id
DELETE /boards/:id
```

### Todos
```
GET    /todos/boards/:boardId/todos
POST   /todos/boards/:boardId/todos
PUT    /todos/:id
DELETE /todos/:id
```

---

## 👨‍💻 Author

Chitranjan Singh  

---

## Screenshots
<img width="1919" height="851" alt="Screenshot 2026-01-30 101052" src="https://github.com/user-attachments/assets/5b276608-feba-4ec1-952e-95ebd87560cf" />
<img width="1901" height="1025" alt="Screenshot 2026-01-30 101125" src="https://github.com/user-attachments/assets/6108cf12-9564-4ad3-bdb3-cde9afc20395" />
