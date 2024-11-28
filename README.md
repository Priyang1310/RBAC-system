
# **Authentication & Role-Based Access Control (RBAC) System**

---

## **Overview**

This project implements a **secure and modular Authentication and Authorization system with Role-Based Access Control (RBAC)** using the **MERN stack**. It demonstrates the ability to manage user roles (e.g., Admin, User, Moderator) and provides fine-grained control over resource access based on these roles.

### **Features**

- **Authentication**:
  - User registration with secure password hashing.
  - User login with JWT-based authentication.
  - User logout with local token removal.

- **Authorization**:
  - Role-Based Access Control (RBAC) to protect sensitive routes.
  - Middleware to restrict access to resources based on roles.

- **Frontend**:
  - Responsive and user-friendly interface for login, registration, and protected dashboard.
  - Role-protected routes with redirection for unauthorized access.

---

## **Tech Stack**

### **Backend**
- **Node.js**: Runtime environment for server-side JavaScript.
- **Express.js**: Web framework for handling routes and middleware.
- **MongoDB**: Database for storing user data.
- **JWT (JSON Web Token)**: For secure token-based authentication.
- **bcrypt.js**: For password hashing.

### **Frontend**
- **React.js**: Framework for building the user interface.
- **Axios**: For making HTTP requests.
- **CSS**: For styling the application.

---

## **Setup Instructions**

### **Backend**

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd backend
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Create `.env` file**:
   Add the following to your `.env` file:
   ```env
   PORT=5000
   MONGO_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/<dbname>?retryWrites=true&w=majority
   JWT_SECRET=your_jwt_secret_key
   NODE_ENV=development
   ```

4. **Run the server**:
   ```bash
   npm start
   ```

---

### **Frontend**

1. **Navigate to the frontend directory**:
   ```bash
   cd auth-rbac-client
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Start the React app**:
   ```bash
   npm start
   ```

---

## **Usage**

### **Authentication**
1. **Register**:
   - Access the registration page.
   - Enter your username, email, and password to create an account.

2. **Login**:
   - Login with valid credentials to access the dashboard.

3. **Role-Based Access**:
   - Users with specific roles can access specific parts of the application.

4. **Logout**:
   - Click the logout button to securely terminate the session.

---

## **Folder Structure**

### **Backend**
```
backend/
├── config/
│   └── db.js
├── middleware/
│   ├── authMiddleware.js
│   └── roleMiddleware.js
├── models/
│   └── User.js
├── routes/
│   └── authRoutes.js
├── server.js
├── package.json
└── .env
```

### **Frontend**
```
auth-rbac-client/
├── src/
│   ├── components/
│   │   ├── Login.js
│   │   ├── Register.js
│   │   ├── Dashboard.js
│   │   └── ProtectedRoute.js
│   ├── styles/
│   │   ├── Login.css
│   │   ├── Register.css
│   │   └── Dashboard.css
│   ├── App.js
│   ├── App.css
│   └── index.js
├── package.json
└── public/
```

---

## **Endpoints**

### **Authentication**
| Method | Endpoint             | Description          |
|--------|-----------------------|----------------------|
| POST   | `/api/auth/register` | Register a new user. |
| POST   | `/api/auth/login`    | Login a user.        |

### **Authorization**
| Method | Endpoint             | Description                               |
|--------|-----------------------|-------------------------------------------|
| GET    | `/api/dashboard`     | Access dashboard (Role-protected route). |

---

## **Contact**
For any queries or feedback, please contact:
- **Name**: Priyang Desai
- **Email**: priyang.r.desai@gmail.com
