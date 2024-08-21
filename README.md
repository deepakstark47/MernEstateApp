# Full-Stack Estate Application

## Overview

This is a full-stack web application designed for estate management, featuring a frontend client, backend API, and real-time socket communication. The application enables users to register, create posts, chat in real-time, and manage their profiles.

## Prerequisites

Ensure you have the following installed:

- Node.js
- npm (Node Package Manager)

## Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/your-username/full-stack-estate.git
   cd full-stack-estate
   ```

2. **Install dependencies for the API**:

   ```bash
   cd api
   npm install
   ```

3. **Install dependencies for the Client**:

   ```bash
   cd ../client
   npm install
   ```

4. **Install dependencies for the Socket**:

   ```bash
   cd ../socket
   npm install
   ```

## Database Setup

1. Set up your database (PostgreSQL, MySQL, etc.) and configure the connection in `prisma/schema.prisma`.
2. Run migrations to set up the database schema:

   ```bash
   npx prisma migrate dev
   ```

## Running the Application

1. **Start the API**:

   ```bash
   cd api
   npm start
   ```

2. **Start the Client**:

   ```bash
   cd ../client
   npm start
   ```

3. **Start the Socket Server**:

   ```bash
   cd ../socket
   npm start
   ```

The application should now be running, with the API on `http://localhost:5000`, the client on `http://localhost:3000`, and the socket server on the configured port.

## Features

- User authentication and authorization.
- Real-time chat functionality.
- Post creation and management.
- User profile management.
- Responsive design with React.
