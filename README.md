# STOCKLY

STOCKLY is a full-stack stock market application split into three main components: a Node.js/Express backend, a main frontend (React), and a dedicated dashboard (React + Material UI).

## Project Structure

- `/backend`: Node.js, Express, MongoDB (Mongoose) backend API.
- `/frontend`: Main user-facing React application.
- `/dashboard`: A React application featuring a user dashboard with charts (Chart.js) and Material UI components.

## Prerequisites

- [Node.js](https://nodejs.org/)
- [MongoDB](https://www.mongodb.com/) (Local instance or MongoDB Atlas)

## Setup Instructions

You will need to run the backend and the frontend/dashboard applications in separate terminal windows.

### 1. Backend Setup

1. Open a terminal and navigate to the backend directory:
   ```bash
   cd backend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file in the `backend` directory and add your MongoDB connection string and preferred port:
   ```env
   MONGO_URL=mongodb://localhost:27017/stockly  # Replace with your MongoDB URI
   PORT=3002
   ```
4. Start the backend server:
   ```bash
   npm start
   ```
   *The server will start on port 3002 (or the port specified in your `.env` file).*

### 2. Frontend Setup

1. Open a new terminal and navigate to the frontend directory:
   ```bash
   cd frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the React app:
   ```bash
   npm start
   ```

### 3. Dashboard Setup

1. Open another terminal and navigate to the dashboard directory:
   ```bash
   cd dashboard
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the dashboard app:
   ```bash
   npm start
   ```

## Pending Work / TODOs

Based on the current codebase, here are the areas that require attention:

- **Database Seeding & Route Cleanup:** The `backend/index.js` contains commented-out routes (`/addHoldings`, `/addPositions`) that contain mock data. These should be moved to a dedicated database seeding script or fully implemented as secure endpoints.
- **Authentication Integration:** The backend `package.json` includes `passport` and `passport-local-mongoose`, but authentication logic is currently missing from `index.js`. This needs to be implemented to secure the APIs.
- **Application Consolidation:** The `frontend` and `dashboard` are currently separate React applications. They should either be integrated into a single application using React Router or clearly separated by role (e.g., landing page vs. logged-in user area).
- **CSS Refinement:** There is a minor `/* TODO */` comment in `dashboard/src/index.css` (line 820) around the `.list li::before` pseudo-element that needs to be addressed.
