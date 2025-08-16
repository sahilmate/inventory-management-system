# Inventory Management System

A full-stack MERN (MongoDB, Express.js, React.js, Node.js) application for managing inventory, users, and transactions with role-based access and email notifications.

---

## Features

- User registration, login, email verification, and password reset
- Role-based access (admin/user)
- Admin dashboard for managing products and categories
- Product search, filtering, and cart/checkout workflow
- Transaction history and order summary
- Automated email notifications (registration, password reset)
- RESTful API with JWT authentication
- Docker Dev Container support for consistent development

---

## Technologies Used

- **Frontend:** React.js, HTML5, CSS3, JavaScript
- **Backend:** Node.js, Express.js, MongoDB, Mongoose
- **Authentication:** JWT, bcrypt
- **Email:** Nodemailer (Gmail SMTP)
- **Dev Environment:** Docker, VS Code Dev Containers

---

## Getting Started

### Prerequisites

- Node.js (v14+)
- MongoDB (local or Atlas)
- (Optional) Docker & VS Code Dev Containers

### Installation

1. **Clone the repository:**
   ```sh
   git clone <your-repo-url>
   cd InventoryManagement-Team-01
   ```

2. **Backend setup:**
   ```sh
   cd 04_BACKEND
   npm install
   # Create a .env file (see .env.example for reference)
   node index.js
   ```

3. **Frontend setup:**
   ```sh
   cd ../03_FRONTEND
   npm install
   # Create a .env file with:
   # REACT_APP_BACKEND_URL=http://localhost:5000/api
   npm start
   ```

4. **(Optional) Dev Container:**
   - Open the project in VS Code
   - Run “Dev Containers: Reopen in Container” from the Command Palette

---

## Environment Variables

**Backend (`04_BACKEND/.env`):**
```
PORT=5000
MONGO_URL=mongodb://localhost:27017/inventory_management
JWT_SECRET=your_jwt_secret
EMAIL_USER=your_gmail@gmail.com
EMAIL_PASS=your_gmail_app_password
```

**Frontend (`03_FRONTEND/.env`):**
```
REACT_APP_BACKEND_URL=http://localhost:5000/api
```

---

## Usage

- Register as a user and verify your email.
- To make an admin, update the user’s `roles` field in MongoDB to `1`.
- Admins can add/edit/delete products and categories.
- Users can browse, search, add to cart, and checkout products.

---

## Project Structure

```
InventoryManagement-Team-01/
  01_UX/           # UI assets (HTML, CSS, JS, images)
  02_ERD_API/      # API/ERD documentation
  03_FRONTEND/     # React frontend
  04_BACKEND/      # Node.js/Express backend
  .devcontainer/   # Dev container config
  README.md
  .gitignore
```

