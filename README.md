# Spring Boot User Management Demo

## 📌 Overview

This project is a beginner-friendly **Spring Boot** application that demonstrates:
- Core Spring concepts: annotations, dependency injection, and inversion of control.
- Layered MVC architecture using model, repository, and service components.
- Unit testing with JUnit 5.
- Git version control with a Gitflow-based workflow.

This version uses an in-memory repository to simulate database operations, making it ideal for learning and prototyping.

---

## 🚀 Technologies Used

- **Java 17**
- **Spring Boot**
- **Gradle**
- **JUnit 5**

---

## 📂 Project Structure
spring-boot-user-demo/
│
├── src/
│ ├── main/java/com/example/demo/
│ │ ├── DemoApplication.java # Main class annotated with @SpringBootApplication
│ │ ├── model/User.java # User model with id, name, surname
│ │ ├── repo/FakeRepoInterface.java # Declares insert, find, delete methods
│ │ ├── repo/FakeRepo.java # Implements in-memory repository logic
│ │ ├── service/UserService.java # Service interface for business logic
│ │ ├── service/UserServiceImpl.java # Implements UserService with dependency injection
│ └── test/java/com/example/demo/
│ └── service/UserServiceTests.java # Unit tests for service methods
│
├── build.gradle
├── README.md


---

🚀 How to Run This Project
✅ Prerequisites
Before running this project, ensure you have the following installed on your system:
1. Java Development Kit (JDK) 21 or higher
Download from:
Oracle JDK
OpenJDK
Verify installation:
java -version
Expected output (example):

nginx
openjdk version "21.0.2" 2024-01-16


2. **Clone the repository**
   Click to open: 👉 [https://github.com/Mkhulekani/springboot-demo.git](https://github.com/Mkhulekani/springboot-demo.git)

   ```bash
   git clone https://github.com/Mkhulekani/springboot-demo.git
   cd springboot-demo
   ```

3. **Run the application**

   ```bash
   ./gradlew bootRun
   ```

   You’ll see printed output in the console from service interactions like user added, removed, or retrieved.

---

### ✅ How to Test

To execute unit tests:

`''''''
./gradlew test
```

> This runs JUnit 5 test cases for `addUser`, `getUser`, and `removeUser` methods in the `UserService`.

---

📌 Features Implemented

✅ MVC Layered Architecture
✅ Constructor-based Dependency Injection (@Autowired)
✅ Spring Boot annotations: @SpringBootApplication, @Override, etc.
✅ In-memory data handling via custom repository
✅ Clean, testable, and modular code
✅ Gitflow workflow for collaborative development

🧪 Code Quality & Testing Standards
Descriptive commit messages using types: feat, fix, test, docs
Follows Java naming conventions and OOP principles (encapsulation, abstraction)
Includes unit tests for edge cases and method accuracy
Uses constructor injection instead of direct instantiation

🌱 Gitflow Branching Strategy
Branch	Purpose
main	Production-ready code
develop	Integration of new features
feature/*	Individual features
test	Pre-merge test validation

Workflow Example:

git checkout -b feature/add-user-service
git commit -m "feat: add user service implementation"
git push origin feature/add-user-service

📚 Resources
Spring Boot Annotations – Baeldung
Spring vs Spring Boot – DZone
Spring Dependency Injection – Baeldung
Spring Boot Tutorial – TutorialsPoint



