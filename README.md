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

## 🧰 How to Run

1. Clone the repository:

```bash
git clone https://github.com/your-username/spring-boot-user-demo.git
cd spring-boot-user-demo

2. 🧰 How to Run Application
./gradlew bootRun

3. You’ll see printed output in the console from service interactions.

✅ How to Test
To execute unit tests:
./gradlew test
