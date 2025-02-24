# Chatter

## Overview
This is a real-time chat application built using the MERN (MongoDB, Express, React, Node.js) stack with Socket.io for real-time communication. Users can send and receive messages instantly.

## Features
- User authentication (JWT-based)
- Real-time messaging using Socket.io
- Group and private chat functionality
- Online/offline status tracking
- Typing indicators
- Responsive UI built with React and TailwindCSS
- MongoDB for storing user and message data

## Tech Stack
- **Frontend:** React, Zustand, TailwindCSS
- **Backend:** Node.js, Express.js
- **Database:** MongoDB (Mongoose)
- **Real-time Communication:** Socket.io
- **Authentication:** JWT (JSON Web Token)

## Installation

### Prerequisites
- Node.js installed
- MongoDB installed and running

### Setup
1. **Clone the repository**
   ```sh
   git clone https://github.com/FazeZxc/chatter.git
   cd chatter
   ```

2. **Install dependencies**
   ```sh
   # Install server dependencies
   npm install

   # Install client dependencies
   cd ../frontend
   npm install
   ```

3. **Set up environment variables**
   Create a `.env` file in the `root` directory and add the following:
   ```env
   PORT=your_port_number
   MONGO_DB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   ```

4. **Run the application**
   ```sh
   # Start backend server
   npm run server

   # Start frontend client
   cd ../client
   npm start
   ```

## API Endpoints
### Authentication
- `POST /api/auth/signup` - Register a new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/logout` - Logout user
- `GET /api/auth/me` - Get authenticated user details

### Messages
- `POST /api/messages` - Send a message
- `GET /api/messages/:chatId` - Get messages for a specific chat

### Users
- `GET /api/users` - Get all users

## WebSocket Events
- `connection` - Establish a connection
- `joinRoom` - Join a chat room
- `sendMessage` - Send a message
- `receiveMessage` - Receive a message
- `disconnect` - Handle disconnection

## Contribution
Feel free to contribute to this project by creating a pull request.

## License
This project is licensed under the MIT License.