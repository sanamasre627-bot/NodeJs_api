# 🔐 Simple Node.js Authentication API

A lightweight, file-based RESTful authentication API for your Flutter applications. No database required - perfect for prototypes and small projects.

![Node.js](https://img.shields.io/badge/Node.js-20-green?style=for-the-badge&logo=node.js)
![Express](https://img.shields.io/badge/Express-4.18-gray?style=for-the-badge&logo=express)
![JWT](https://img.shields.io/badge/JWT-Auth-orange?style=for-the-badge&logo=jsonwebtokens)

## 🚀 Quick Start

### 1. Clone & Setup
```bash
git clone https://github.com/yourusername/simple-auth-api.git
cd simple-auth-api
npm install
```

### 2. Run the Server
```bash
npm run dev
```

### 3. Test API
```bash
# Health check
curl http://localhost:5000/api/health
```

## 📡 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/health` | Server status check |
| `POST` | `/api/auth/register` | Create new user account |
| `POST` | `/api/auth/login` | User login with JWT token |
| `GET` | `/api/auth/me` | Get user profile (protected) |

## 🔑 Usage Examples

### Register User
```bash
curl -X POST http://localhost:5000/api/auth/register \
  -H "Content-Type: application/json" \
  -d '{
    "name": "John Doe",
    "email": "john@example.com",
    "password": "123456"
  }'
```

### Login User
```bash
curl -X POST http://localhost:5000/api/auth/login \
  -H "Content-Type: application/json" \
  -d '{
    "email": "john@example.com",
    "password": "123456"
  }'
```

### Get Profile
```bash
curl -X GET http://localhost:5000/api/auth/me \
  -H "Authorization: Bearer YOUR_JWT_TOKEN"
```

## 🛠️ Features

- ✅ **User Registration** with password hashing
- ✅ **Secure Login** with JWT tokens
- ✅ **Protected Routes** with auth middleware
- ✅ **File-based Storage** - no database needed
- ✅ **CORS Enabled** for Flutter apps
- ✅ **Error Handling** and validation

## 📁 Project Structure

```
simple-auth-api/
├── server.js          # Main server file
├── package.json       # Dependencies
├── database.json      # Auto-created data storage
└── README.md          # This file
```

## 🚀 Deployment

### Local Development
```bash
npm run dev
```

### Production
```bash
npm start
```

## 🔧 Technologies Used

- **Express.js** - Web framework
- **JWT** - Authentication tokens
- **bcryptjs** - Password hashing
- **CORS** - Cross-origin requests

## 🤝 Contributing

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

### ⭐ Star this repo if you found it helpful!

**Happy Coding!** 🚀

</div>
