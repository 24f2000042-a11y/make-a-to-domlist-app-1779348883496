# Todo List App (MERN)

## Overview
A simple, modern **Todo List** web application built with the MERN stack (MongoDB, Express, React, Node). The UI follows a clean **Modern Blue** theme and works on desktop and mobile.

## Features
- Create, read, update (toggle complete), and delete todos.
- Responsive design.
- RESTful API with Express.
- Data persisted in MongoDB.
- Axios for client‑side HTTP requests.

## Project Structure

root/
├─ backend/            # Express API
│   ├─ server.js
│   ├─ package.json
│   └─ .env.example
└─ frontend/           # React + Vite
    ├─ src/
    │   ├─ App.jsx
    │   ├─ App.css
    │   └─ main.jsx
    ├─ index.html
    └─ package.json


## Prerequisites
- Node.js (v18 or later)
- npm or yarn
- MongoDB Atlas account (or local MongoDB instance)

## Setup
### 1. Clone the repository
bash
git clone <repo-url>
cd <repo-folder>


### 2. Backend
bash
cd backend
npm install   # or yarn
cp .env.example .env
# Edit .env and add your MongoDB connection string
npm run dev   # starts server on PORT (default 5000)

The API will be available at `http://localhost:5000/api`.

### 3. Frontend
bash
cd ../frontend
npm install   # or yarn
# Create a .env file for Vite (optional)
# VITE_API_URL defaults to http://localhost:5000
npm run dev   # Vite dev server, usually http://localhost:5173

Open the URL shown in the terminal to use the app.

### 4. Production Build
bash
# Backend
cd backend
npm start   # ensure PORT env matches your hosting setup

# Frontend
cd ../frontend
npm run build   # generates dist/ folder
# Serve the static files with any static server or integrate with Express if desired.


## API Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET    | `/api/todos` | Get all todos |
| POST   | `/api/todos` | Create a todo (`{ text: "..." }`) |
| PUT    | `/api/todos/:id` | Update fields (e.g., `{ completed: true }`) |
| DELETE | `/api/todos/:id` | Delete a todo |

## Environment Variables
- **MONGO_URI** – MongoDB connection string.
- **PORT** – Port for Express server (default 5000).
- **VITE_API_URL** – (frontend) Base URL for API calls; defaults to `http://localhost:5000`.

## License
This project is open‑source and free to use.
