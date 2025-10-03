# Learning Management System (LMS) Frontend

## Overview

This is the **frontend of a Learning Management System (LMS)** built with **React, Vite, and Tailwind CSS**. It allows students to view courses, assignments, quizzes, certificates, and track progress. Admins can manage courses, students, and view leaderboards (backend integration required).

**Technologies used:**

* React (functional components + hooks)
* React Router DOM for page navigation
* Tailwind CSS for styling
* Vite for development and build

---

## Features

* Responsive **UI** with Tailwind CSS
* Pages:

  * Home
  * Dashboard
  * Course Details
  * Assignments
  * Quizzes
  * Leaderboard
  * Certificates
  * Login / Register
* React Router for **client-side routing**
* Ready to integrate with **MERN backend** (MongoDB, Express, Node.js)
* JWT-based authentication support (backend required)

---

## Folder Structure

```
lms-frontend/
├─ public/
│   └─ index.html
├─ src/
│   ├─ assets/
│   ├─ components/
│   │   └─ Navbar.jsx
│   ├─ pages/
│   │   ├─ Home.jsx
│   │   ├─ Dashboard.jsx
│   │   ├─ CourseDetails.jsx
│   │   ├─ Assignments.jsx
│   │   ├─ Quizzes.jsx
│   │   ├─ Leaderboard.jsx
│   │   ├─ Certificates.jsx
│   │   ├─ Login.jsx
│   │   └─ Register.jsx
│   ├─ App.jsx
│   ├─ main.jsx
│   └─ index.css
├─ package.json
├─ tailwind.config.js
├─ postcss.config.js
└─ README.md
```

---

## Installation

### Prerequisites

* Node.js v18+
* npm v9+

### Steps

1. Clone the repo:

```bash
git clone <your-repo-url>
cd lms-frontend
```

2. Install dependencies:

```bash
npm install
```

3. Start the development server:

```bash
npm run dev
```

4. Open the app in your browser at:

```
http://localhost:5173/
```

---

## Tailwind CSS Setup

If Tailwind CSS is not working, ensure `tailwind.config.js` exists with:

```js
export default {
  content: ["./index.html", "./src/**/*.{js,jsx,ts,tsx}"],
  theme: { extend: {} },
  plugins: [],
};
```

Include Tailwind in `src/index.css`:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

---

## Routing (React Router)

`App.jsx` uses **React Router DOM v6**:

```jsx
import { BrowserRouter as Router, Routes, Route } from "react-router-dom";
import Home from "./pages/Home";
import Dashboard from "./pages/Dashboard";
import CourseDetails from "./pages/CourseDetails";
import Assignments from "./pages/Assignments";
import Quizzes from "./pages/Quizzes";
import Leaderboard from "./pages/Leaderboard";
import Certificates from "./pages/Certificates";
import Login from "./pages/Login";
import Register from "./pages/Register";
import Navbar from "./components/Navbar";

function App() {
  return (
    <Router>
      <Navbar />
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/dashboard" element={<Dashboard />} />
        <Route path="/course/:id" element={<CourseDetails />} />
        <Route path="/assignments" element={<Assignments />} />
        <Route path="/quizzes" element={<Quizzes />} />
        <Route path="/leaderboard" element={<Leaderboard />} />
        <Route path="/certificates" element={<Certificates />} />
        <Route path="/login" element={<Login />} />
        <Route path="/register" element={<Register />} />
      </Routes>
    </Router>
  );
}

export default App;
```

---

## Screenshots (Optional)

Add screenshots of your pages here, e.g., Home, Dashboard, Leaderboard, etc.

---

## Future Enhancements

* Integrate **backend with MongoDB, Node.js, and Express**
* JWT authentication and user roles (Admin / Student)
* File upload for courses and assignments
* Progress tracking and leaderboards in real-time
* Responsive mobile-friendly design

---

## License

This project is **open-source**. You can use and modify it for educational purposes.
