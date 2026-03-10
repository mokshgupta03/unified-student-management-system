# 🎓 Unified Student Life Management System

A full-stack web application to help students manage academics, health, and personal finance in one place.

## 🚀 Tech Stack
- **Frontend:** HTML, CSS, JavaScript, Chart.js
- **Backend:** Node.js, Express
- **Database:** MongoDB
- **Auth:** JWT + bcrypt

---

## 📁 Project Structure
```
project/
├── frontend/
│   ├── index.html        # Login / Register
│   ├── dashboard.html    # Main dashboard
│   ├── academics.html    # Academics module
│   ├── health.html       # Health tracker
│   ├── finance.html      # Finance tracker
│   ├── profile.html      # Profile settings
│   └── style.css         # Global styles
└── backend/
    ├── server.js
    ├── .env
    ├── routes/
    ├── controllers/
    ├── models/
    └── middleware/
```

---

## ⚙️ Prerequisites

Make sure you have installed:
- [Node.js](https://nodejs.org/) (v16 or higher)
- [MongoDB](https://www.mongodb.com/try/download/community) (running locally on port 27017)

---

## 🛠️ How to Run

### Step 1 – Install MongoDB
Download and install MongoDB Community Edition. Start the MongoDB service:
- **Windows:** MongoDB runs as a service automatically after install. Or run: `net start MongoDB`

### Step 2 – Start the Backend
```bash
cd backend
npm install
node server.js
```
You should see:
```
✅ MongoDB Connected Successfully
🚀 Server running on http://localhost:5000
```

### Step 3 – Open the Frontend
Open the `frontend/index.html` file in your browser, **or** use VS Code Live Server extension.

> ✅ Recommended: Use [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) in VS Code for hot-reload.

---

## 🔑 Default API Endpoints

| Module | Method | Endpoint |
|--------|--------|----------|
| Auth | POST | `/api/auth/register` |
| Auth | POST | `/api/auth/login` |
| Auth | GET | `/api/auth/profile` |
| Dashboard | GET | `/api/dashboard` |
| Academics | GET/POST | `/api/academics/subjects` |
| Academics | GET/POST | `/api/academics/assignments` |
| Academics | GET/POST | `/api/academics/study-plans` |
| Academics | GET | `/api/academics/gpa` |
| Health | POST | `/api/health/log` |
| Health | GET | `/api/health/weekly` |
| Finance | GET/POST | `/api/finance/expenses` |
| Finance | GET/POST | `/api/finance/income` |
| Finance | GET/POST | `/api/finance/budget` |
| Finance | GET | `/api/finance/summary` |

---

## 🔧 Environment Variables (backend/.env)
```
MONGO_URI=mongodb://localhost:27017/student_life
JWT_SECRET=studentlife_supersecret_jwt_key_2024
PORT=5000
```

---

## 🌐 Deployment

### Frontend → Netlify
1. Drag & drop the `frontend/` folder to [Netlify Drop](https://app.netlify.com/drop)
2. Update `API` variable in each HTML file to your Render backend URL

### Backend → Render
1. Push your `backend/` folder to GitHub
2. Create new Web Service on [Render](https://render.com)
3. Set environment variables (MONGO_URI, JWT_SECRET)
4. Build command: `npm install`, Start command: `node server.js`

### Database → MongoDB Atlas
1. Create free cluster at [MongoDB Atlas](https://cloud.mongodb.com)
2. Create a database user
3. Get connection string and set it as `MONGO_URI` in Render environment variables

---

## ✨ Features
- ✅ JWT Authentication (Register/Login)
- ✅ Academic task management with GPA calculator
- ✅ Health tracker with Chart.js weekly analytics
- ✅ Personal finance tracker with pie & bar charts
- ✅ Budget planning with progress tracker
- ✅ Dark glassmorphism UI
- ✅ Mobile responsive design
- ✅ Smart health reminders
