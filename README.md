<div align="center">

# 🚀 Spring Boot JWT Authentication & Authorization REST API

### Secure Authentication using Spring Security | JWT | BCrypt | MySQL | Flyway

![Java](https://img.shields.io/badge/Java-21-orange?style=for-the-badge&logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-4.x-6DB33F?style=for-the-badge&logo=springboot)
![Spring Security](https://img.shields.io/badge/Spring-Security-success?style=for-the-badge)
![JWT](https://img.shields.io/badge/JWT-Authentication-purple?style=for-the-badge)
![MySQL](https://img.shields.io/badge/MySQL-Database-4479A1?style=for-the-badge&logo=mysql)
![Hibernate](https://img.shields.io/badge/Hibernate-ORM-59666C?style=for-the-badge&logo=hibernate)
![Flyway](https://img.shields.io/badge/Flyway-Migrations-CC0200?style=for-the-badge)
![Maven](https://img.shields.io/badge/Maven-Build-C71A36?style=for-the-badge&logo=apachemaven)

**A production-ready RESTful API implementing secure JWT Authentication & Authorization using Spring Security, BCrypt password encryption, MySQL, Hibernate ORM, and Flyway database migrations.**

</div>

---

# 📌 Project Overview

This project was developed as part of the **Prodigy InfoTech Internship – Task 3: JWT Authentication & Authorization**.

The application extends the previous CRUD REST API by integrating **Spring Security** and **JSON Web Tokens (JWT)** to secure all protected endpoints.

Users can register, securely log in, receive a JWT access token, and access protected APIs only after successful authentication. Passwords are encrypted using **BCrypt** before being stored in the MySQL database.

The project follows Spring Boot best practices with a layered architecture, making it scalable and production-ready.

---

# ✨ Features

- ✅ User Registration
- ✅ User Login
- ✅ JWT Authentication
- ✅ Spring Security Integration
- ✅ BCrypt Password Encryption
- ✅ Stateless Authentication
- ✅ Protected REST APIs
- ✅ User CRUD Operations
- ✅ Spring Data JPA
- ✅ Hibernate ORM
- ✅ MySQL Integration
- ✅ Flyway Database Migration
- ✅ DTO Validation
- ✅ Global Exception Handling
- ✅ UUID Primary Keys
- ✅ Password Hidden from API Responses

---

# 🛠 Tech Stack

| Technology | Purpose |
|------------|---------|
| Java 21 | Programming Language |
| Spring Boot | Backend Framework |
| Spring Security | Authentication & Authorization |
| JWT | Token-Based Authentication |
| Spring Data JPA | Data Access Layer |
| Hibernate | ORM Framework |
| MySQL | Relational Database |
| Flyway | Database Migration |
| BCrypt | Password Encryption |
| Maven | Dependency Management |
| Postman | API Testing |
| IntelliJ IDEA | Development Environment |

---

# 🏗 Project Architecture

```text
                    Client (Postman)
                           │
                           ▼
                 Authentication Controller
                           │
                           ▼
                Authentication Service
                           │
                           ▼
                BCrypt Password Encoder
                           │
                           ▼
                  User Repository (JPA)
                           │
                           ▼
                    Hibernate ORM Layer
                           │
                           ▼
                     MySQL Database
                           ▲
                           │
                 JWT Authentication Filter
                           │
                           ▼
                  Protected REST APIs
```

---

# 📂 Project Structure

```text
basic-rest-api
│
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com.example.basic_rest_api
│   │   │
│   │   ├── config
│   │   ├── controller
│   │   ├── dto
│   │   ├── exception
│   │   ├── model
│   │   ├── repository
│   │   ├── security
│   │   ├── service
│   │   └── BasicRestApiApplication
│   │
│   │   └── resources
│   │       ├── application.properties
│   │       └── db
│   │           └── migration
│
├── pom.xml
├── README.md
└── .gitignore
```

---

# 🔐 JWT Authentication Flow

```text
              Register User
                    │
                    ▼
      Password Encrypted using BCrypt
                    │
                    ▼
          Stored in MySQL Database
                    │
                    ▼
               User Login
                    │
                    ▼
          Credentials Verified
                    │
                    ▼
            JWT Token Generated
                    │
                    ▼
      Authorization: Bearer <TOKEN>
                    │
                    ▼
      JWT Authentication Filter
                    │
                    ▼
      Access Protected REST APIs
```

---

# 🗄 Database Details

| Property | Value |
|----------|-------|
| Database | MySQL |
| ORM | Hibernate |
| Repository | Spring Data JPA |
| Migration Tool | Flyway |
| Password Encryption | BCrypt |
| Primary Key | UUID |

---

# 🔗 REST API Endpoints

## Authentication APIs

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | `/auth/register` | Register User |
| POST | `/auth/login` | Login User |

---

## Protected User APIs

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | `/api/users` | Retrieve All Users |
| GET | `/api/users/{id}` | Retrieve User by ID |
| POST | `/api/users` | Create User |
| PUT | `/api/users/{id}` | Update User |
| DELETE | `/api/users/{id}` | Delete User |

---

# 🧪 Sample API Requests

## Register User

```http
POST /auth/register
```

```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "age": 24,
  "password": "password123"
}
```

---

## Login

```http
POST /auth/login
```

```json
{
  "email": "john@example.com",
  "password": "password123"
}
```

---

## Login Response

```json
{
  "token": "eyJhbGciOiJIUzI1NiJ9..."
}
```

---

## Access Protected Endpoint

```http
GET /api/users
```

Header:

```text
Authorization: Bearer <JWT_TOKEN>
```

---

# ⚙️ How to Run the Project

## Clone Repository

```bash
git clone https://github.com/uddishasinghh31/YOUR_REPOSITORY_NAME.git
```

---

## Configure MySQL

```sql
CREATE DATABASE prodigy_task3_db;
```

---

## Update application.properties

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/prodigy_task3_db
spring.datasource.username=YOUR_USERNAME
spring.datasource.password=YOUR_PASSWORD

jwt.secret=YOUR_SECRET_KEY
jwt.expiration=86400000
```

---

## Run the Project

```bash
mvn spring-boot:run
```

Or run:

```
BasicRestApiApplication.java
```

The application will start on:

```
http://localhost:8080
```

---

# 🔒 Security Features

- BCrypt Password Encryption
- JWT Authentication
- Stateless Session Management
- Spring Security Integration
- JWT Authentication Filter
- Protected Endpoints
- Secure Password Storage
- UUID-Based Primary Keys
- DTO Validation
- Global Exception Handling

---

# 🚀 Future Improvements

- Refresh Token Support
- Role-Based Authorization (Admin/User)
- Swagger / OpenAPI Documentation
- Docker Containerization
- Unit & Integration Testing
- GitHub Actions CI/CD
- Cloud Deployment (AWS / Railway / Render)

---

# 👩‍💻 Author

**Udisha Singh**

Backend Developer | Java | Spring Boot | MySQL

Linkedin: https://www.linkedin.com/in/udisha-singh-47170b338 

---

# 📄 Internship Details

**Organization:** Prodigy InfoTech

- **Task 1:** Build a REST API for CRUD Operations
- **Task 2:** Integrate Persistent Storage using MySQL, Spring Data JPA, Hibernate, and Flyway
- **Task 3:** Implement JWT-Based Authentication & Authorization using Spring Security and JSON Web Tokens

---

<div align="center">

### ⭐ If you found this project useful, please consider giving it a Star!

</div>
