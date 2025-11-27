Mini Question Manager – Full Stack Application

A full-stack Question & Answer Manager built using **React**, **Node.js**, **Express**, and **MongoDB**, deployed on **Netlify** and **Render**.
This project allows users to create, view, update, and delete interview-style questions across different technical categories.

This project is submitted as part of **ProU Technology – Online Assessment (Frontend + Backend + Full-stack Development Track)**.

---

Live Demo

 Frontend (Netlify)

https://mini-question-manager.netlify.app

Backend API (Render)

https://mini-question-manager.onrender.com

---

 Tech Stack

### **Frontend**

* React (CRA)
* React Router
* Axios
* CSS (custom)

**Backend**

* Node.js
* Express.js
* Mongoose (MongoDB ORM)
* MongoDB Atlas
* CORS

### **Deployment**

* Netlify (Frontend)
* Render (Backend)
* GitHub (Version Control)

---

Features

Core Features

* Add new questions with topic + question + answer
* Fetch all questions from database
* View single question
* Update question
* Delete question
* Fully responsive UI

 Frontend Highlights

* Clean and minimal UI
* React Router based navigation
* API integration using Axios
* Environment–based API configuration (`REACT_APP_SERVER_URL`)

Backend Highlights

* RESTful API design
* MongoDB CRUD operations
* Modular route + controller structure
* CORS enabled for production

Bonus Implementations

* Deployed both frontend & backend
* Clean API handling
* Organized folder structure
* Reusable components & modular code


Project Structure


Mini-Question-Manager
│
├── client/                 # React Frontend
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── api.js
│   │   └── App.js
│   └── package.json
│
├── server/                 # Node + Express Backend
│   ├── controllers/
│   ├── db/
│   ├── routes/
│   ├── models/
│   └── server.js
│
└── README.md




Installation & Setup Guide

Follow these steps to run the project locally.

---

Clone the Repository**

```bash
git clone https://github.com/Rishigupta7190/Mini-Question-Manager.git
cd Mini-Question-Manager
```

---

# **Backend Setup (server/)**

Go to server folder**

```bash
cd server
```

Install dependencies**

```bash
npm install
```

Create a `.env` file**

Add your MongoDB connection string:

```
MONGO_URL=your_mongodb_connection_url
```

Start backend**

```bash
npm start
```

Backend will run on:

```
http://localhost:8000
```

---

# **Frontend Setup (client/)**

Go to client folder**

```bash
cd ../client
```

 Install dependencies**

```bash
npm install
```

Create a `.env` file**

```
REACT_APP_SERVER_URL=http://localhost:8000/api/v1
```

For production (Netlify):

```
REACT_APP_SERVER_URL=https://mini-question-manager.onrender.com/api/v1
```

Start frontend**

```bash
npm start
```

Frontend runs on:

```
http://localhost:3000
```

---

API Documentation

### **Base URL**

```
https://mini-question-manager.onrender.com/api/v1
```

### **Endpoints**

| Method | Endpoint         | Description           |
| ------ | ---------------- | --------------------- |
| POST   | `/createpost`    | Create a new question |
| GET    | `/getposts`      | Fetch all questions   |
| GET    | `/getsinglepost` | Fetch one question    |
| PUT    | `/updatepost`    | Update question       |
| DELETE | `/deletepost`    | Delete question       |

---

Screenshots (Add later)

You can add 2–3 screenshots here:

```
/screenshots
   - home.png
   - create.png
   - update.png
```

(Upload screenshots on GitHub → copy image link → paste here.)

---

Contact

**Rishi Gupta**
B.Tech CSE – VIT Vellore
Email: *[guptarishi5959@gmail.com](mailto:guptarishi5959@gmail.com)*
GitHub: *github.com/Rishigupta7190*


