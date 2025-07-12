# 🛡️ SpringSecurity Demo

A beginner-friendly Spring Boot application that demonstrates **Spring Security** with form-based login and Thymeleaf integration. It uses default authentication and auto-generates a login password at runtime.

---

## ✨ Features

### 🔐 Spring Security
- Default login form provided by Spring Security.
- Auto-generated password printed in the console on startup.
- Basic in-memory authentication for quick setup and testing.

### 🌐 Web Support
- Uses **Spring Boot Web Starter** for creating REST endpoints or MVC-style pages.
- Thymeleaf is integrated for server-side HTML rendering.

### 🧪 Testing
- Includes support for unit and integration testing using Spring Boot Test and Spring Security Test.

---

## 🧱 Project Structure

```
SpringSecurity.demo/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com.example.SpringSecurity.demo/
│   │   │       └── Application.java
│   │   └── resources/
│   │       ├── application.properties
│   │       └── templates/           # Thymeleaf HTML templates
├── pom.xml                          # Maven configuration
```

---

## ⚙️ Configuration

### 🔑 Default Login Credentials

```txt
Username: user
Password: (auto-generated at runtime, check console logs)
```

To override the default, add the following to `application.properties`:
```properties
spring.security.user.name=admin
spring.security.user.password=admin123
```

---

## 🧩 Dependencies Used

These dependencies are included in `pom.xml`:

| Dependency                          | Purpose                                                        |
|-------------------------------------|----------------------------------------------------------------|
| spring-boot-starter-web             | Core web starter (Spring MVC + embedded Tomcat)               |
| spring-boot-starter-security        | Enables Spring Security for authentication & authorization     |
| spring-boot-starter-thymeleaf       | Integrates Thymeleaf templating engine                         |
| thymeleaf-extras-springsecurity6    | Thymeleaf support for Spring Security tags                     |
| spring-boot-starter-test            | Provides testing framework with JUnit, Mockito, etc.           |
| spring-security-test                | Adds testing support for security features                     |

---

## 🚀 How to Run the Project

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/SpringSecurity.demo.git
cd SpringSecurity.demo
```

### 2. Run the App
Using Maven wrapper:
```bash
./mvnw spring-boot:run
```
Or with installed Maven:
```bash
mvn spring-boot:run
```

---

## 🛠️ Optional DB Configuration

*(Only required if you connect to a database — not required for basic security demo)*

### Configure your DB credentials in `src/main/resources/application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/your_db_name
spring.datasource.username=YOUR_DB_USERNAME
spring.datasource.password=YOUR_DB_PASSWORD
spring.jpa.hibernate.ddl-auto=update
```

---

## 🧪 Testing

Run unit and integration tests using:
```bash
mvn test
```

---

## 📄 License

This project is licensed under the MIT License. You are free to use, modify, and distribute it.
