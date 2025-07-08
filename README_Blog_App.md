
# 📝 Blog App Backend - Spring Boot

A RESTful Blog Application built using **Spring Boot**, featuring **JWT-based authentication**, **role-based authorization**, **pagination**, **DTO architecture**, and **MySQL** database. API documentation is integrated with **Swagger**.

## 🚀 Features

- ✅ User Registration & Login (JWT Authentication)
- 🔒 Role-Based Authorization (Admin, Editor, Reader)
- 📚 CRUD operations for:
  - Posts
  - Categories
  - Comments
- 📤 Upload & Retrieve Images
- 📑 DTO-Based API Responses
- 🔄 Pagination and Sorting
- 📊 Swagger UI API Documentation

---

## 🧱 Tech Stack

| Layer        | Technology                          |
|--------------|--------------------------------------|
| Language     | Java 17+                             |
| Framework    | Spring Boot, Spring MVC              |
| Security     | Spring Security, JWT (JSON Web Tokens) |
| ORM          | Spring Data JPA (Hibernate)          |
| Database     | MySQL                                |
| API Docs     | Swagger (OpenAPI)                    |
| JSON Mapper  | Jackson                              |
| Build Tool   | Maven                                |

---

## 📁 Project Structure

```bash
src
├── main
│   ├── java/com/example/blogapp
│   │   ├── controller
│   │   ├── service
│   │   ├── repository
│   │   ├── model
│   │   ├── payload (DTOs)
│   │   ├── config (Security, JWT)
│   │   └── exception
│   └── resources
│       ├── application.properties
│       └── static/
```

---

## ⚙️ Configuration

### `application.properties`
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/blogdb
spring.datasource.username=root
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

jwt.secret=your_jwt_secret
jwt.expiration=3600000

springdoc.api-docs.enabled=true
```

---

## 🔐 Authentication & Roles

- **JWT Token** generated during login
- Use token in `Authorization: Bearer <token>` header for secured routes
- Roles: `ROLE_ADMIN`, `ROLE_USER`

---

## 🛠️ API Endpoints (Sample)

| Method | Endpoint                | Description              |
|--------|-------------------------|--------------------------|
| POST   | `/api/auth/register`    | Register new user        |
| POST   | `/api/auth/login`       | Login & get JWT token    |
| GET    | `/api/posts`            | Get all posts (paginated)|
| POST   | `/api/posts`            | Create a post (Admin only)|
| DELETE | `/api/posts/{id}`       | Delete a post (Admin only)|
| GET    | `/swagger-ui/index.html`| Open Swagger API docs    |

---

## 🧪 Testing with Swagger

Once app is running:

- Visit: `http://localhost:8080/swagger-ui/index.html`
- Try out all secured and open endpoints
- Provide `Bearer <token>` for secured routes

---

## 📦 Run the App

```bash
# Clone the repository
git clone https://github.com/your-username/blog-app-springboot.git
cd blog-app-springboot

# Run via Maven
./mvnw spring-boot:run
```

---

## 👨‍💻 Author

**Eklavya Singh**  
Bachelor of Technology – Computer Science  
📫 `seklavya.work@gmail.com`  
🌐 [GitHub Profile](https://github.com/EKlavyasing)  
🔗 [LinkedIn](https://www.linkedin.com/in/eklavya-singh10/)

---
