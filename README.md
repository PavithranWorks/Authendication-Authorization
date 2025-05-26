## Authentication & Authorization

This is a secure Node.js REST API for user authentication and password reset functionality using **Express**, **MongoDB**, **bcrypt**, and **JWT**. It includes endpoints for user registration, login, password recovery, and reset. Environment variables are used for configuration.

---

## ✨ Features

- 🔐 User Signup & Signin
- 🔄 Forgot Password & Secure Reset
- 🔑 JWT-based Authentication
- 🧊 Hashed Passwords using bcrypt
- 📧 Email Notifications via Nodemailer
- 🛡️ Input Validation
- 🌐 CORS enabled

---

## 🧰 Technologies Used

- Node.js
- Express.js
- MongoDB & Mongoose
- JSON Web Tokens (JWT)
- bcryptjs
- nodemailer
- dotenv
---

## 📁 Project Structure

```

project-root/
│
├── routes/
│   └── auth.js           # Authentication routes
├── models/
│   └── User.js           # Mongoose User schema
├── controllers/
│   └── authController.js # Logic for auth routes
├── utils/
│   └── emailService.js   # Nodemailer configuration
├── .env                  # Environment variables
├── server.js             # Entry point
├── package.json
└── README.md

````

---


### 📝 Auth Routes

| Method | Endpoint                 | Description               |
| ------ | ------------------------ | ------------------------- |
| POST   | `/api/auth/signup`       | Register a new user       |
| POST   | `/api/auth/signin`       | Login an existing user    |
| POST   | `/api/auth/forgot`       | Request password reset    |
| POST   | `/api/auth/reset/:token` | Reset password with token |

---

## 🛡️ Security Practices

* Environment variables are used to protect sensitive data.
* Passwords are hashed using `bcryptjs` before storage.
* JWT is used to manage sessions securely.
* Secrets are not hardcoded and `.env` is listed in `.gitignore`.

---



---

## 📬 Forgot Password Flow

1. User requests password reset via `/api/auth/forgot`.
2. Receives a secure token link via email.
3. Resets password using `/api/auth/reset/:token`.

---

## 🧾 License

This project is licensed under the MIT License. Feel free to use and modify it for your projects.

---

