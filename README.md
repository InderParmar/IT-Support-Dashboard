# **IT Support Dashboard**

The **IT Support Dashboard** is a web application designed for efficient ticket management and IT support operations. It allows users to create tickets, IT assistants to manage and escalate tickets, IT technicians to resolve tickets, and IT admins to view comprehensive ticket histories and manage roles. The application is built using the MERN (MongoDB, Express, React, Node.js) stack and styled with Tailwind CSS.

---

## **Features**

### **Backend**
- User Authentication with JWT
  - Register and login functionality.
  - Role-based access control (`user`, `assistant`, `technician`, `admin`).
- Ticket Management
  - Create, update, and manage ticket statuses.
  - Add comments to tickets.
  - View ticket history by user.
- API Routes
  - Secure and RESTful API endpoints for users, tickets, and comments.
- MongoDB for database storage with Mongoose schemas.

### **Frontend**
- Tailwind CSS for responsive design and styling.
- Role-based dashboards with React Router for navigation.
- Login page with form validation and authentication.
- Axios integration for API calls with token-based authentication.

---

## **Tech Stack**

### **Frontend**
- React
- Tailwind CSS
- Axios
- React Router DOM

### **Backend**
- Node.js
- Express.js
- MongoDB (with Mongoose)
- JSON Web Token (JWT)
- bcrypt.js

---

## **Installation**

### **Clone the Repository**
```bash
git clone https://github.com/your-username/it-support-dashboard.git
cd it-support-dashboard
```

### **Backend Setup**
1. Navigate to the `backend` folder:
   ```bash
   cd backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the `backend` folder and add:
   ```env
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_secret_key
   ```

4. Start the backend server:
   ```bash
   npm start
   ```

### **Frontend Setup**
1. Navigate to the `client` folder:
   ```bash
   cd client
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the `client` folder and add:
   ```env
   REACT_APP_BASE_URL=http://localhost:5001
   ```

4. Start the frontend server:
   ```bash
   npm start
   ```

---

## **Usage**

1. Open the application in your browser:
   - Frontend: [http://localhost:3000](http://localhost:3000)
   - Backend: [http://localhost:5001](http://localhost:5001)

2. **User Roles and Permissions**:
   - **General Users**: Create and view tickets.
   - **IT Assistants**: Update ticket statuses, add comments, and escalate tickets.
   - **IT Technicians**: Resolve escalated tickets and leave resolution comments.
   - **IT Admins**: View all tickets, manage users, and generate reports.

3. **Test API Endpoints**:
   - Use [Postman](https://www.postman.com/) or [cURL](https://curl.se/) for testing backend API routes.

---

## **Folder Structure**

### **Backend**
```
backend/
├── models/        # Mongoose schemas for Users, Tickets, and Comments
├── routes/        # API routes
├── .env           # Environment variables
├── server.js      # Express server
```

### **Frontend**
```
client/
├── src/
│   ├── components/    # Reusable components
│   ├── pages/         # Pages for routing
│   ├── services/      # API service integration
│   ├── App.js         # Main app component
│   ├── index.css      # Tailwind CSS setup
│   └── index.js       # React entry point
├── .env               # Environment variables
```

---

## **API Endpoints**

### **Users**
- `POST /api/users/register`: Register a new user.
- `POST /api/users/login`: Login and receive a JWT token.

### **Tickets**
- `POST /api/tickets`: Create a new ticket.
- `PATCH /api/tickets/:id/status`: Update ticket status.
- `GET /api/tickets/history`: Get ticket history for a user.

### **Comments**
- `POST /api/comments`: Add a comment to a ticket.
- `GET /api/comments/:ticketId`: Get all comments for a ticket.

---

## **Contributing**

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m "Add new feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.

---

## **License**

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## **Acknowledgments**
- Built with the MERN stack for full-stack development.
- Styled using Tailwind CSS for a modern, responsive design.
- Thanks to the open-source community for inspiring this project.

---
