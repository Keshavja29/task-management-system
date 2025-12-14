# Task Management System

[![Backend API](https://img.shields.io/badge/Backend-Live-success?style=for-the-badge&logo=render)](https://task-management-system-oafy.onrender.com)

## 🌐 **LIVE BACKEND API**
**🚀 [Backend API](https://task-management-system-oafy.onrender.com)** - Node.js + Express + MongoDB

> **Note:** Frontend deployment coming soon!

---

A full-stack task management application built with React, Node.js, Express, and MongoDB.

## Features

- **User Authentication** - JWT-based secure login/signup
- **Task CRUD Operations** - Create, Read, Update, Delete tasks
- **Priority Levels** - High, Medium, Low priority tasks
- **Status Tracking** - Todo, In Progress, Completed
- **Dashboard Analytics** - Visual charts and statistics
- **Responsive Design** - Works on all devices
- **Search & Filter** - Find tasks quickly

## Tech Stack

**Frontend:**
- React.js
- Redux (State Management)
- Axios (API calls)
- Chart.js (Analytics)
- Tailwind CSS

**Backend:**
- Node.js
- Express.js
- MongoDB
- JWT Authentication
- bcrypt (Password hashing)

## Installation

### Backend Setup
```bash
cd backend
npm install
cp .env.example .env
# Add your MongoDB URI and JWT secret
npm start
```

### Frontend Setup
```bash
cd frontend
npm install
npm start
```

## API Endpoints

### Auth
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user

### Tasks
- `GET /api/tasks` - Get all tasks
- `POST /api/tasks` - Create new task
- `PUT /api/tasks/:id` - Update task
- `DELETE /api/tasks/:id` - Delete task

## Environment Variables

```
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
PORT=5000
```

## Screenshots

[Add screenshots here]

## Future Enhancements

- Team collaboration features
- File attachments
- Email notifications
- Calendar integration
- Mobile app

## License

MIT License

---

**Made with ❤️ by Keshav** | [Backend API](https://task-management-system-oafy.onrender.com)
