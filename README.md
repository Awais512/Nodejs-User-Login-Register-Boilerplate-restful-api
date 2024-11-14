# Node.js User Authentication Boilerplate 🔐

A robust Node.js REST API boilerplate with MongoDB for user authentication and role-based authorization. Features include user registration, login, profile management, and admin capabilities.

## ⚡ Features

- User authentication (Register/Login)
- JWT-based authorization
- Role-based access control (Admin/User)
- Profile management
- Protected routes middleware
- MongoDB integration
- Express.js REST API
- Error handling
- Input validation

## 🛠️ Tech Stack

- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM
- **JWT** - Authentication
- **bcrypt** - Password hashing
- **dotenv** - Environment management

## 🚀 Quick Start

### Prerequisites

- Node.js installed
- MongoDB installed locally or MongoDB Atlas account
- Postman (for testing APIs)

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/nodejs-user-login-register-boilerplate.git
cd nodejs-user-login-register-boilerplate
```

2. Install dependencies
```bash
npm install
```

3. Configure environment variables
```bash
# Create a .env file in the root directory
cp .env.example .env

# Add your configurations
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
PORT=5000
```

4. Start the server
```bash
npm start
```

## 📡 API Endpoints

### Authentication Routes
```bash
POST /api/users/register - Register a new user
POST /api/users/login - Login user
```

### Protected User Routes
```bash
GET /api/users/profile - Get user profile
PUT /api/users/profile - Update user profile
```

### Protected Admin Routes
```bash
GET /api/admin/users - Get all users (Admin only)
DELETE /api/admin/users/:id - Delete user (Admin only)
```

## 🔑 Authentication Flow

### Register User
```bash
POST /api/users/register
Content-Type: application/json

{
    "name": "John Doe",
    "email": "john@example.com",
    "password": "123456"
}
```

### Login User
```bash
POST /api/users/login
Content-Type: application/json

{
    "email": "john@example.com",
    "password": "123456"
}
```

### Authorization
```bash
# Include the JWT token in request headers
Authorization: Bearer <your_jwt_token>
```

## 🛡️ Middleware

### Authentication Middleware
- Verifies JWT tokens
- Handles token expiration
- Validates user sessions

### Role-based Middleware
- `protectRoute` - Ensures user authentication
- `adminRoute` - Ensures admin privileges

## 📁 Project Structure
```
├── config/
│   ├── db.js
│   └── config.js
├── middleware/
│   ├── authMiddleware.js
│   └── adminMiddleware.js
├── models/
│   └── User.js
├── routes/
│   ├── userRoutes.js
│   └── adminRoutes.js
├── controllers/
│   ├── userController.js
│   └── adminController.js
├── utils/
│   └── generateToken.js
├── .env
├── server.js
└── package.json
```

## 🔧 Configuration

### Environment Variables
```env
NODE_ENV=development
PORT=5000
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
```

## 🚦 Error Handling

The API implements comprehensive error handling for:
- Invalid routes
- Authentication errors
- Database errors
- Validation errors
- Server errors

## 🔒 Security Features

- Password hashing using bcrypt
- JWT-based authentication
- Protected routes
- Role-based access control
- Input validation
- HTTP headers security

## 🧪 Testing

```bash
# Run tests
npm test

# Run tests with coverage
npm run test:coverage
```

## 📝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

## 🤝 Support

Give a ⭐️ if this project helped you!

---

Made with ❤️ by Awais Raza
