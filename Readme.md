
# Password Reset Flow - Backend

This is the Node.js and Express backend for handling user registration, login, and password reset flows with email verification.

## 🔧 Technologies Used

- Node.js
- Express.js
- MongoDB & Mongoose
- dotenv
- bcryptjs
- nodemailer
- JWT

## 🔐 Routes

| Method | Endpoint                                | Description                        |
|--------|------------------------------------------|------------------------------------|
| POST   | /api/auth/register                      | Register a new user                |
| POST   | /api/auth/login                         | Login a user                       |
| POST   | /api/auth/forgot-password               | Send reset link via email         |
| POST   | /api/auth/reset-password/:id/:token     | Reset user password                |

## 📁 Folder Structure

backend/
│
├── Controllers/
│ └── authController.js
│
├── Models/
│ └── User.js
│
├── Routers/
│ └── authRoute.js
│
├── Database/
│ └── dbConfig.js
│
├── index.js
└── .env

## Configure environment variables in .env:

PORT=3000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
BASE_URL=http://localhost:5173
EMAIL_USER=your_email@example.com
EMAIL_PASS=your_email_password

## 📝 Notes

The backend uses JWT tokens embedded in reset email links.

Passwords are hashed with bcrypt.

Emails are sent via NodeMailer with the link to reset the password.

## POSTMAN Collection

https://documenter.getpostman.com/view/39965124/2sB2x6nYDd

