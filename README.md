# Task 1: Zenith - A Full-Stack Blog Application
Zenith is a feature-rich, full-stack blog platform built from the ground up with a custom Google OAuth 2.0 authentication system. This project demonstrates a comprehensive understanding of modern web development, from backend architecture and database management to frontend state handling and a polished UI/UX.

## 🔴 Live Demo
You can view and test the live, deployed application here:

[https://zenith-lilac.vercel.app/](https://zenith-lilac.vercel.app/)

## ⭐ Important Note on Data Persistence

This application's backend is deployed on Render's free tier, which uses an ephemeral filesystem. This means that the server's local file storage (the db.json file that acts as the database) will reset after a period of inactivity (approximately 15 minutes).

What this means for the demo:

- Any posts, comments, or likes you create on the live site will disappear after the server goes to sleep and wakes up again.
- This is an expected behavior of the free hosting platform and not a bug in the application's code.

## 📸 Screenshots

<img width="1892" height="868" alt="image" src="https://github.com/user-attachments/assets/bb22a7c1-7097-4ae7-9832-26c18faa5ad3" />
<img width="1872" height="876" alt="image" src="https://github.com/user-attachments/assets/6228dfe7-5f28-4c34-855d-551d721e2044" />


## ✨ Features
**Custom Google OAuth 2.0:** Secure user login and session management handled manually without Firebase/Supabase.

**Full CRUD for Posts:** Logged-in users can Create, Read, Update, and Delete their own posts.

**Interactive Engagement:** Users can Like/Unlike and Comment on any post.

**User Dashboard:** A dedicated page for users to view all their posts, liked posts, and comments in one place.

**Responsive UI/UX:** A modern, dark-themed, and fully responsive design built with Tailwind CSS using a custom color palette.

**Local JSON Database:** Utilizes a lightweight, local db.json file for data persistence, making setup incredibly simple and reliable.

## 🛠️ Tech Stack
**Frontend:** React, Vite, Tailwind CSS

**Backend:** Node.js, Express.js

**Database:** LowDB (for local JSON file-based storage)

**Authentication:** Custom Google OAuth 2.0 flow with JSON Web Tokens (JWT)

## 🚀 Setup and Installation
To run this project locally, follow these steps:

**1. Clone the Repository**
```bash
git clone [https://github.com/itsmyra1006/Zenith.git](https://github.com/itsmyra1006/Zenith.git)
cd Zenith
``` 

**2. Backend Setup**
```bash
# Navigate to the server directory
cd server
# Install dependencies
npm install

# Create the .env file and add your credentials (see below)
# On Windows: copy .env.example .env
# On Mac/Linux: cp .env.example .env

# Start the server
npm run dev
```
```bash
3. Frontend Setup
# Navigate to the client directory (from the root of Task-1-Zenith-Blog-App)
cd client

# Install dependencies
npm install

# Create the .env file (see below)
# On Windows: copy con .env and paste the variable
# On Mac/Linux: touch .env

# Start the client
npm run dev
```

## ⚙️ Environment Variables
You will need to create two .env files with the following variables for the application to run.

**Backend** (/server/.env)
Create this file by copying .env.example
```bash
# Google OAuth 2.0 Credentials
GOOGLE_CLIENT_ID=YOUR_GOOGLE_CLIENT_ID_HERE
GOOGLE_CLIENT_SECRET=YOUR_GOOGLE_CLIENT_SECRET_HERE

# JSON Web Token Secret (use a long, random string)
JWT_SECRET=YOUR_CUSTOM_JWT_SECRET_KEY_HERE

# The root URL of your backend server
SERVER_ROOT_URI=http://localhost:5000

# The root URL of your frontend application
UI_ROOT_URI=http://localhost:5173
``` 

**Frontend** (/client/.env)
Create this file manually

```bash
# Google Client ID (must be exposed to the client)
VITE_GOOGLE_CLIENT_ID=YOUR_GOOGLE_CLIENT_ID_HERE
```
