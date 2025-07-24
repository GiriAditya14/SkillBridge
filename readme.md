## SkillBridge : Real-Time Microlearning Platform for Underserved Communities
A full-stack web application connecting students from underprivileged backgrounds with mentors for instant doubt-solving sessions through real-time Q&A, video calls, AI chatbot fallback, and feedback.

---

## Features

## User Authentication
- Role-based access (Student/Teacher)
- JWT authentication
- Protected routes

## Doubt Management
- Students can submit doubts (text + image upload)
- Teachers can view and accept open doubts
- Real-time updates using Socket.io

## Feedback System
- Students can rate mentors post-session (1-5 stars)
- Teachers can view their feedback statistics
- Average rating calculation

## Video Calling
- Integrated with ZEGO Cloud
- Real-time 1:1 video communication
- Screen sharing capability

## AI Chatbot (Fallback Support)
- Gemini AI-powered chatbot for instant query resolution
- Available when no teacher is online
- Trained to give contextual, helpful answers

---

### Video Demo
<a href=""><img src="https://imgs.search.brave.com/H330hjXg0E35DY7KPYi5ItE21yGS7qaIlfM-HpFD67Q/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly91cGxv/YWQud2lraW1lZGlh/Lm9yZy93aWtpcGVk/aWEvY29tbW9ucy9m/L2ZkL1lvdVR1YmVf/ZnVsbC1jb2xvcl9p/Y29uXygyMDI0KS5z/dmc" width="50"></a>

---

## Tech Stack

### Frontend
- React.js
- Tailwind CSS
- Axios
- React Router
- Socket.io-client
- ZEGO Express Engine

### Backend
- Node.js
- Express.js
- MongoDB & Mongoose
- JWT
- Socket.io
- Gemini AI API

---

## Installation Guide

### Prerequisites
- Node.js (v14+)
- MongoDB
- ZEGO Developer Account
- Gemini AI API Key

## Backend Setup

### Clone the repository:

```bash
git clone https://github.com/KanakGupta1208/hack.git
cd education/server

```
    
### Install dependencies:

  ```bash
  npm install

  ```
### Create .env file:
```env
MONGO_URI=mongodb://localhost:27017/SkillBridge
JWT_SECRET=your_jwt_secret_here
PORT=5000
ZEGO_APP_ID=your_zego_app_id
ZEGO_SERVER_SECRET=your_zego_server_secret
GEMINI_API_KEY=your_gemini_api_key
```
### Start the backend server:

```bash
npm run dev
```

## Frontend Setup
### Navigate to frontend directory:
```bash

cd ../SkillBridge
```

### Install dependencies:
```bash
npm install
```

### Create .env file:
```env

REACT_APP_API_BASE_URL=http://localhost:5000
REACT_APP_ZEGO_APP_ID=your_zego_app_id
REACT_APP_ZEGO_SERVER_SECRET=your_zego_server_secret
```

Start the frontend development server:

```bash
npm run dev
```

## Project Structure

### Backend (server/)
```
root
├── models/           # MongoDB schemas
│   ├── Feedback.js
│   ├── Question.js
│   └── User.js
├── routes/           # API endpoints
│   ├── auth.js
│   ├── feedback.js
│   ├── question.js
│   ├── teacher.js
│   └── zego.js
├── middleware/       # Authentication middleware
│   └── authMiddleware.js
├── server/
    └── index.js          # Server entry point
```

### Frontend (SkillBridge/frontend/src/)
```
src/
├── components/
│   ├── Auth/         # Login/Register forms
│   ├── Feedback/     # Feedback components
│   ├── Questions/    # Doubt submission and management UI
│   ├── VideoCall/    # Video call interface
│   └── Layout/       # Reusable layout components
├── context/          # Authentication context
├── hooks/            # Custom React hooks
├── pages/            # Route pages
├── services/         # API communication services
└── App.jsx           # Main application file
```

---

## 👥 Team
- Aditya Giri – Handled backend development, database modeling, API integration, and route protection.
- Kanak Gupta – Contributed to frontend development with responsive design, route integration, state management and page optimizations.
- Chaitanya Sharma – Managed backend deployment and ensured smooth coordination under pressure.
- Aadarsh Dangi – Handled frontend development and UI design.

---

## 📃 License
Licensed under the MIT License.

---

## 🤝 Acknowledgements
- MNNIT Allahabad for hosting Hack36 8.0
- Hackathon Mentors and Judges for valuable feedback
