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

The application extends the previous CRUD REST API by implementing **Spring Security** and **JSON Web Tokens (JWT)** to secure all protected endpoints.

Users can register, securely log in, receive a JWT token, and access protected APIs only after successful authentication.

Passwords are encrypted using **BCrypt** before being stored in the MySQL database, ensuring secure credential management and production-ready authentication practices.

---

# ✨ Features

- ✅ User Registration
- ✅ User Login
- ✅ JWT Token Generation
- ✅ Spring Security Integration
- ✅ BCrypt Password Encryption
- ✅ Protected REST APIs
- ✅ Stateless Authentication
- ✅ JWT Authentication Filter
- ✅ CRUD Operations
- ✅ MySQL Integration
- ✅ Hibernate ORM
- ✅ Spring Data JPA
- ✅ Flyway Database Migration
- ✅ UUID Primary Keys
- ✅ Request Validation
- ✅ Global Exception Handling
- ✅ Password Hidden from API Responses

---

# 🛠 Tech Stack

| Technology | Purpose |
|------------|---------|
| Java 21 | Programming Language |
| Spring Boot | Backend Framework |
| Spring Security | Authentication & Authorization |
| JWT | Secure Authentication |
| Spring Data JPA | Database Access |
| Hibernate | ORM Framework |
| MySQL | Relational Database |
| Flyway | Database Version Control |
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

                   JWT Authentication

                            │

                            ▼

                  Protected REST APIs
```

---

# 📂 Project Structure

```text
basic-rest-api
│
├── docs
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
└── .env (ignored)
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
          Stored inside MySQL Database
                    │
                    ▼
               User Login Request
                    │
                    ▼
            Credentials Validated
                    │
                    ▼
            JWT Token Generated
                    │
                    ▼
      Client Stores the JWT Token
                    │
                    ▼
 Authorization: Bearer <JWT_TOKEN>
                    │
                    ▼
      JWT Authentication Filter
                    │
                    ▼
        Token Validation Successful
                    │
                    ▼
        Access Protected Endpoints
```

---

# 🗄 Database Details

**Database:** MySQL

**ORM:** Hibernate (Spring Data JPA)

**Migration Tool:** Flyway

**Password Encryption:** BCrypt

**Primary Key:** UUID

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

## Configure Environment Variables

Create a `.env` file in the project root.

```properties
DB_URL=jdbc:mysql://localhost:3306/prodigy_task3_db
DB_USERNAME=your_username
DB_PASSWORD=your_password

JWT_SECRET=your_secret_key
JWT_EXPIRATION=86400000
```

---

## Run the Application

Using Maven

```bash
mvn spring-boot:run
```

or simply run

```
BasicRestApiApplication.java
```

---

# 📸 Project Screenshots

## 🏗 Project Structure

Shows the layered package structure used in the application.

<p align="center">
<img src="./git_structure.png" width="400"/>
</p>

---

## 📂 Complete Project Directory

Displays the complete Maven project structure.

<p align="center">
<img src="./complete-project-structure.png" width="400"/>
</p>

---

## 🚀 Server Running Successfully

<p align="center">
<img src="./01-server-running.png" width="400"/>
</p>

---

## ➕ Create User

<p align="center">
<img src="./02-create-user.png" width="400"/>
</p>

---

## 📋 Get All Users

<p align="center">
<img src="./03-get-all-users.png" width="400"/>
</p>

---

## 🔍 Get User By ID

<p align="center">
<img src="./04-get-user-by-id.png" width="400"/>
</p>

---

## ✏️ Update User

<p align="center">
<img src="./05-update-user.png" width="400"/>
</p>

---

## 🗑 Delete User

<p align="center">
<img src="./06-delete-user.png" width="400"/>
</p>

---

## ❌ Validation Error (Bad Request)

<p align="center">
<img src="./07-bad-request.png" width="400"/>
</p>

---

## ⚠️ User Not Found

<p align="center">
<img src="./08-user-not-found.png" width="400"/>
</p>

---

## 🔑 User Login

Successful login using registered credentials.

<p align="center">
<img src="./login_user.png" width="400"/>
</p>

---

## 🎫 JWT Token Generated

JWT token returned after successful authentication.

<p align="center">
<img src="./pass_security.png" width="400"/>
</p>

---

## 🔒 Protected API Without Token (403 Forbidden)

Access denied when JWT token is not provided.

<p align="center">
<img src="./access_withoutToken.png" width="400"/>
</p>

---

## ✅ Protected API With Valid JWT Token

Protected endpoint accessed successfully using Bearer Token.

<p align="center">
<img src="./access_withToken.png" width="400"/>
</p>

---

## 🗄 MySQL Database

Stored user records inside MySQL.

<p align="center">
<img src="./mysql_database.png" width="400"/>
</p>

---

## 📊 Data Retrieved from Database

Users fetched successfully from MySQL.

<p align="center">
<img src="./get_fromDatabase.png" width="400"/>
</p>

---

## 🔐 Password Stored as BCrypt Hash

Passwords are encrypted before being stored.

<p align="center">
<img src="./sql_updated_pass.png" width="400"/>
</p>

---

## 🛡 Flyway Migration History

Automatic schema versioning using Flyway.

<p align="center">
<img src="./flyway_schema.png" width="400"/>
</p>

---

# 🧪 Sample Login Response

```json
{
  "token": "eyJhbGciOiJIUzI1NiJ9..."
}
```

---

# 🔒 Security Features

- BCrypt Password Encryption
- Spring Security Integration
- JWT Authentication
- Stateless Session Management
- Protected REST Endpoints
- JWT Authentication Filter
- Password Hidden from API Responses
- UUID-based Primary Keys
- DTO Validation
- Global Exception Handling

---

# 🚀 Future Improvements

- Refresh Tokens
- Role-Based Authorization
- Swagger / OpenAPI Documentation
- Docker Support
- Unit Testing (JUnit & Mockito)
- Integration Testing
- Logging using SLF4J
- GitHub Actions CI/CD
- Cloud Deployment (AWS / Railway / Render)

---

# 👩‍💻 Author

**Udisha Singh**

Backend Developer | Java | Spring Boot | MySQL

GitHub: https://github.com/uddishasinghh31

---

# 📄 Internship Details

**Organization:** Prodigy InfoTech

**Task 1:** Build a REST API for CRUD Operations

**Task 2:** Integrate Persistent Storage using MySQL, Spring Data JPA, Hibernate, and Flyway

**Task 3:** Implement JWT-based Authentication & Authorization using Spring Security and JSON Web Tokens

---

<div align="center">

## ⭐ If you found this project useful, please consider giving it a Star!

</div>
