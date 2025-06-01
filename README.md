# Funchat

Simple MERN chat app — minimal, private, and fast.

Author: Susheel Kumar

## Repo layout
- backend/ — Express + Socket.IO API (entry: [backend/server.js](backend/server.js))
- frontend/ — React + Chakra UI client (entry: [frontend/src/index.js](frontend/src/index.js))
- frontend/src/components — UI components (examples: [Signup](frontend/src/components/Authentication/Signup.js), [ProfileModal](frontend/src/components/miscellaneous/ProfileModal.js))

## Features
- Real-time messaging with Socket.IO
- Group and 1:1 chats
- User authentication with JWT
- File upload (profile pictures)
- Responsive UI built with Chakra UI

## Tech stack
- Node.js, Express, Socket.IO
- MongoDB (Mongoose)
- React, Chakra UI

## Quickstart (development)

1. Install root dependencies
   - From project root:
     sudo apt update
     cd /home/yashpatil/projects/mern-chat-app
     npm install

2. Backend
   - Install backend deps (already in root)
     npm run server
   - Or run directly:
     node backend/server.js
   - Backend entry: [backend/server.js](backend/server.js)

3. Frontend
   - Open a new terminal:
     cd /home/yashpatil/projects/mern-chat-app/frontend
     npm install
     npm start
   - Frontend proxy is configured in [frontend/package.json](frontend/package.json)

4. Open the app
   - Client: http://localhost:3000
   - API: http://localhost:5000 (default)

## Environment variables
Create a `.env` in `backend/` with at least:
- PORT=5000
- MONGO_URI=your_mongo_connection_string
- JWT_SECRET=your_jwt_secret

## Build for production
From project root:
npm run build
This script builds the frontend and prepares the repo for deployment.

## Useful files
- Backend server/socket setup: [backend/server.js](backend/server.js)
- Frontend theme and provider: [frontend/src/index.js](frontend/src/index.js)
- Authentication pages: [frontend/src/components/Authentication/Login.js](frontend/src/components/Authentication/Login.js), [frontend/src/components/Authentication/Signup.js](frontend/src/components/Authentication/Signup.js)
- Chat rendering: [frontend/src/components/ScrollableChat.js](frontend/src/components/ScrollableChat.js)
