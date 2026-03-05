# Jira Clone (SaaS Project Management Platform)

A full-stack project management and collaboration platform inspired by Jira and Trello. This application enables teams to seamlessly manage workspaces, track tasks across Kanban boards, and collaborate in real-time.

---

## 🚀 Features

### **Authentication & Role Management**
*   Secure **JWT-based** authentication (Register, Login, Session Management).
*   Role-based access control (Admin, User).
*   Encrypted passwords using `bcryptjs`.

### **Workspace & Project Organization**
*   Create distinct projects/workspaces.
*   Manage team members within each project.
*   Customized project keys (e.g., `PR-1`, `TASK-5`) and branding colors.

### **Real-Time Kanban Board**
*   Interactive drag-and-drop task management powered by `@hello-pangea/dnd`.
*   **Real-time synchronization** across all connected clients via `Socket.IO`. (If user A moves a task to 'Done', user B sees it instantly without refreshing).
*   Columns for `To Do`, `In Progress`, and `Done` statuses.

### **Advanced Task Management**
*   Create, view, edit, and delete tasks.
*   Assign tasks to specific team members.
*   Visual indicators for task priorities (`Low`, `Medium`, `High`, `Critical`).
*   Due dates and attachment tracking.

### **Collaboration & Notifications**
*   Real-time commenting system with user avatars and timestamps.
*   Mention users in comments (coming soon).
*   In-app notification system tracking task assignments, updates, and mentions.

---

## 💻 Tech Stack

### **Frontend**
*   **Framework:** React 19 (Vite)
*   **Styling:** Tailwind CSS (Premium Dark Theme with Glassmorphism)
*   **State Management:** Zustand
*   **Routing:** React Router DOM v7
*   **Icons:** Lucide React
*   **HTTP Client:** Axios (with interceptors)
*   **Real-time:** Socket.IO Client
*   **Drag & Drop:** `@hello-pangea/dnd`

### **Backend**
*   **Runtime:** Node.js
*   **Framework:** Express.js
*   **Database:** MongoDB & Mongoose
*   **Authentication:** JSON Web Tokens (JWT)
*   **Real-time:** Socket.IO
*   **Media Storage:** Cloudinary & Multer (Setup for attachments/avatars)
*   **Development:** Nodemon, dotenv

---

## 🛠️ Installation & Setup

### Prerequisites
1.  Node.js installed (v18+ recommended)
2.  MongoDB instance running (Local or MongoDB Atlas)

### 1. Clone & Install Dependencies
First, install dependencies for both the backend and frontend.

```bash
# Install backend dependencies
cd backend
npm install

# Install frontend dependencies
cd ../frontend
npm install
```

### 2. Environment Variables
Create `.env` files in both directories.

**Backend (`backend/.env`):**
```env
NODE_ENV=development
PORT=5001
MONGO_URI=mongodb://localhost:27017/jiraclone  # Or your MongoDB Atlas URI
JWT_SECRET=your_super_secret_jwt_key
JWT_EXPIRE=7d
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
CLIENT_URL=http://localhost:5174
```

**Frontend (`frontend/.env`):**
```env
VITE_API_URL=http://localhost:5001/api
```

### 3. Run the Application
Open two separate terminal windows.

**Terminal 1 (Backend):**
```bash
cd backend
npm run dev
```

**Terminal 2 (Frontend):**
```bash
cd frontend
npm run dev
```

The application should now be running. 
* Frontend: `http://localhost:5174`
* Backend API: `http://localhost:5001`

---

## 📸 Screenshots

*(Replace these with actual screenshots of your application)*
*   **Kanban Board:** Highlighting the drag-and-drop interface.
*   **Task Details:** Showing the commenting system and task metadata.
*   **Dashboard:** Showing the project overview.

---

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page.
# jira
# jira
