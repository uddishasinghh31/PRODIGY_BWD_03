# 🚀 Spring Boot User Management REST API

![Java](https://img.shields.io/badge/Java-21-orange?style=for-the-badge&logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-4.1-green?style=for-the-badge&logo=springboot)
![MySQL](https://img.shields.io/badge/MySQL-8-blue?style=for-the-badge&logo=mysql)
![Hibernate](https://img.shields.io/badge/Hibernate-ORM-brown?style=for-the-badge&logo=hibernate)
![Flyway](https://img.shields.io/badge/Flyway-Migrations-red?style=for-the-badge)
![JWT](https://img.shields.io/badge/JWT-Authentication-purple?style=for-the-badge)
![Spring Security](https://img.shields.io/badge/Spring%20Security-Secured-green?style=for-the-badge)
![Maven](https://img.shields.io/badge/Maven-Build-red?style=for-the-badge&logo=apachemaven)

---

## 📖 Project Overview

This project is a **RESTful User Management API** developed using **Spring Boot** as part of my **Prodigy Infotech Internship**.

The application supports complete CRUD operations along with **JWT-based Authentication & Authorization**, secure password encryption using **BCrypt**, MySQL database integration, Flyway database migrations, request validation, exception handling, and a layered architecture following Spring Boot best practices.

---

# ✨ Features

- ✅ Create User
- ✅ Get All Users
- ✅ Get User by ID
- ✅ Update User
- ✅ Delete User
- ✅ JWT Authentication
- ✅ Spring Security
- ✅ Password Encryption (BCrypt)
- ✅ Protected REST APIs
- ✅ Request Validation
- ✅ Global Exception Handling
- ✅ MySQL Database
- ✅ Hibernate ORM
- ✅ Flyway Database Migration
- ✅ UUID Primary Keys

---

# 🛠 Tech Stack

| Technology | Purpose |
|------------|----------|
| Java 21 | Programming Language |
| Spring Boot | Backend Framework |
| Spring Security | Authentication & Authorization |
| JWT | Secure Authentication |
| Hibernate / JPA | ORM |
| MySQL | Database |
| Flyway | Database Version Control |
| Maven | Dependency Management |
| Postman | API Testing |
| IntelliJ IDEA | IDE |
| Git & GitHub | Version Control |

---

# 📂 Project Structure

```
src
│
├── config
│     └── Security Configuration
│
├── controller
│     ├── AuthController
│     └── UserController
│
├── dto
│     ├── LoginRequest
│     ├── UserRequest
│     └── AuthResponse
│
├── exception
│
├── model
│
├── repository
│
├── security
│     ├── JwtService
│     ├── JwtAuthenticationFilter
│     └── CustomUserDetailsService
│
├── service
│
└── resources
      ├── application.properties
      └── db/migration
```

---

# 🏗 Architecture

```
                    Client
                       │
                    Postman
                       │
                REST Controller
                       │
                    Service Layer
                       │
                 Repository Layer
                       │
              Hibernate (JPA ORM)
                       │
                     MySQL
```

---

# 🔐 Authentication Flow

```
Register User
      │
      ▼
Password encrypted using BCrypt
      │
      ▼
Saved into MySQL Database
      │
      ▼
Login
      │
      ▼
JWT Token Generated
      │
      ▼
Client stores Token
      │
      ▼
Bearer Token sent in Header
      │
      ▼
JWT Filter validates Token
      │
      ▼
Protected APIs Accessible
```

---

# 📌 API Endpoints

## Authentication APIs

| Method | Endpoint | Description |
|----------|----------------|----------------|
| POST | `/auth/register` | Register User |
| POST | `/auth/login` | Login User |

---

## User APIs

| Method | Endpoint |
|----------|----------------|
| GET | `/api/users` |
| GET | `/api/users/{id}` |
| POST | `/api/users` |
| PUT | `/api/users/{id}` |
| DELETE | `/api/users/{id}` |

---

# 🧪 API Testing

All APIs were tested successfully using **Postman**.

### Register User

```
POST /auth/register
```

### Login

```
POST /auth/login
```

Returns

```json
{
  "token":"JWT_TOKEN"
}
```

### Protected Endpoint

```
GET /api/users
```

Requires

```
Authorization

Bearer <JWT_TOKEN>
```

---

# 📷 Screenshots

---

## 🔑 Login API

![Login](login_user.png)

---

## 🎫 JWT Token

![JWT](pass_security.png)

---

## 🔒 Protected API (Without Token)

![403](access_withoutToken.png)

---

## ✅ Protected API (With Token)

![Users](access_withoutToken.png)

---

## 🗄 MySQL Database

![Database](sql_updated_pass.png)

---

## 🛡 Flyway Migration

![Flyway](flyway_schema.png)

---

# 📈 Security Features

- BCrypt Password Encryption
- JWT Authentication
- Stateless Authentication
- Spring Security
- Protected Endpoints
- Password Hidden from API Response
- UUID-based User IDs

---

# 🚀 Future Improvements

- Swagger/OpenAPI Documentation
- Role Based Authorization (Admin/User)
- Refresh Token Support
- Docker Containerization
- Unit Testing (JUnit & Mockito)
- CI/CD using GitHub Actions

---

# ▶️ How to Run

### Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
```

---

### Navigate

```bash
cd basic-rest-api
```

---

### Configure Database

Update:

```
application.properties
```

with your MySQL credentials.

---

### Run Project

```bash
mvn spring-boot:run
```

---

### Access APIs

```
http://localhost:8080
```

---

# 👩‍💻 Author

**Udisha Singh**

Backend Developer | Java | Spring Boot | MySQL

GitHub: https://github.com/uddishasinghh31

---

# ⭐ If you found this project useful, consider giving it a Star!
