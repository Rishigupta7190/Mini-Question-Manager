Mini Question Manager – Full Stack Web Application

A full-stack Question & Answer management application built using **React**, **Node.js**, **Express**, and **MongoDB**.  
Users can create, view, update, and delete interview-style Q&A across different topics like OS, DBMS, DSA, AI, etc.

This project is submitted as part of:

ProU Technology – Online Assessment**  
Track 1 & 2 & 3 – Frontend, Backend & Full-stack Development**



Live Demo Links

Frontend (Netlify)
**Live URL:**  
`https://mini-question-manager.netlify.app/`

Backend API (Vercel)
**Base API URL:**  
`https://YOUR-BACKEND-VERCEL-URL`  
_example: `https://mini-question-manager-api.vercel.app`_

- Health check (root):  
  `GET https://YOUR-BACKEND-VERCEL-URL/`
- API base for frontend:  
  `https://YOUR-BACKEND-VERCEL-URL/api/v1`

The frontend reads the API base from `REACT_APP_SERVER_URL` in `.env`.

GitHub Repository

**Code (Full Stack – client + server):**  
`https://github.com/Rishigupta7190/Mini-Question-Manager`

---

Tech Stack

### Frontend
- React (Create React App)
- React Router
- Axios
- CSS (custom, responsive layout)

### Backend
- Node.js
- Express.js
- Mongoose (MongoDB ODM)
- MongoDB Atlas (cloud database)

### DevOps / Deployment
- Netlify – Frontend hosting
- Vercel – Backend/API hosting
- GitHub – Version control and source code

---

Features

Core Features (Full Stack)

- Create new questions with:
  - Topic (e.g., OS, DBMS, DSA, AI, HR, etc.)
  - Question text
  - Answer text
- View all questions in a clean card-based UI
- View single question details
- Update existing question
- Delete question
- Questions are stored in **MongoDB** and accessed via REST APIs.

Frontend (Track 1 – Web)

- Responsive layout for desktop
- Clear, readable typography
- Simple, intuitive navigation:
  - `/` – Home/List all questions
  - `/createpost` – Add new question
  - `/updatepost/:id` – Edit an existing question (if used)
  - `/:id` – View single question
- API integration using Axios and environment-based configuration.

Backend (Track 2 – API + DB)

- RESTful API architecture with Express
- CRUD operations on a `Post`/Question model:
  - `createpost` – Create new question
  - `getposts` – Get all questions
  - `getsinglepost` – Get details of one question
  - `updatepost` – Update a question
  - `deletepost` – Delete a question
- MongoDB Atlas for persistent storage
- Connection handling and error logging.

Full Stack (Track 3 – Integrated Web + API + DB)

- React frontend consumes Express APIs
- APIs connected to MongoDB Atlas
- Deployed full stack:
  - UI: Netlify
  - API: Vercel
- Environment variables used to separate local and production configurations.

---

API Documentation

**Base URL (production):**

text
https://mini-question-manager.vercel.app/

| Method | Endpoint         | Description             | Request Body (JSON)               |
| ------ | ---------------- | ----------------------- | --------------------------------- |
| POST   | `/createpost`    | Create a new question   | `{ topic, question, answer }`     |
| GET    | `/getposts`      | Get all questions       | –                                 |
| GET    | `/getsinglepost` | Get one question by ID  | Query: `?id=<postId>`             |
| PUT    | `/updatepost`    | Update an existing post | `{ id, topic, question, answer }` |
| DELETE | `/deletepost`    | Delete a question       | Query or body: `id`               |


Example response format:
{
  "success": true,
  "responseData": [
    {
      "_id": "68b7ea7cffaf8605748fb090",
      "topic": "Operating System (OS)",
      "question": "What is the difference between process and thread?",
      "answer": "A process is an independent program...",
      "__v": 0
    }
  ]
}


Local Setup – How to Run the Project
 Clone the repository
git clone https://github.com/Rishigupta7190/Mini-Question-Manager.git
cd Mini-Question-Manager


 Backend Setup (server/)
cd server
npm install


Create a .env file inside server/:

MONGO_URL=your_mongodb_atlas_connection_string
PORT=8000


Start the backend:

npm start


Backend will run on:

http://localhost:8000


Test:

http://localhost:8000/ → health JSON

http://localhost:8000/api/v1/getposts → list of questions



Frontend Setup (client/)

In a new terminal:

cd ../client
npm install


Create .env inside client/:

For local development:

REACT_APP_SERVER_URL=http://localhost:8000/api/v1


For production (Netlify):

REACT_APP_SERVER_URL=https://YOUR-BACKEND-VERCEL-URL/api/v1


Start the React app:

npm start


The frontend will run at:

http://localhost:3000

Screenshots / Demo

