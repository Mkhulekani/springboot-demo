# Spring Boot User Demo - Part 1

## Project Overview

This project is a simple Spring Boot web application demonstrating a basic MVC layered architecture with dependency injection, annotations, and in-memory data storage. It serves as an introduction to fundamental Spring Boot concepts.

**Key Concepts Covered:**

* Spring Boot fundamentals (annotations, Dependency Injection (DI), Inversion of Control (IoC))
* Layered architecture:
    * Model (`User.java`)
    * Repository (FakeRepoInterface.java, FakeRepo.java)
    * Service (UserService.java, UserServiceImpl.java)
    * Controller (optional for advanced learners)
* Object-oriented principles (encapsulation, abstraction)
* Writing clean, testable code
* Git version control and team collaboration using Gitflow branches and commit standards.

🚀 **Technologies Used**

* **Java 17:** The programming language used to build the application.
* **Spring Boot:** A framework that simplifies the development of Java-based enterprise applications.
* **Gradle:** A powerful build automation tool used for managing dependencies and building the project.
* **JUnit 5:** A popular testing framework for writing and running unit tests in Java.

## How to Run the Application

This project is a standard Spring Boot application. You will need the following installed on your system to build and run it:

### Prerequisites

1.  **Java Development Kit (JDK):** Ensure you have a compatible JDK installed. This project uses **Java 17**. You can download it from [Oracle Java Downloads](https://www.oracle.com/java/technologies/downloads/) or an open-source distribution like [OpenJDK](https://openjdk.java.net/).

    * **Verification:** Open your terminal or command prompt and run:
        ```bash
        java -version
        ```
        You should see information about your installed Java version, confirming it's Java 17 or a compatible version.

2.  **Gradle:** This project uses Gradle as its build automation tool. You need to have Gradle installed on your system. You can find installation instructions on the [Gradle website](https://gradle.org/install/).

    * **Verification:** Open your terminal or command prompt and run:
        ```bash
        gradle -v
        ```
        This should display the installed Gradle version.

## Getting Started

1.  **Clone the Repository:**
    ```bash
    git clone <repository_url>
    cd spring-boot-user-demo
    ```
    *(Replace `<repository_url>` with the actual URL of your GitHub repository)*

2.  **Build the Application:**
    Navigate to the project root directory in your terminal and run the Gradle build command:
    ```bash
    gradle build
    ```
    This command will download the necessary dependencies (specified in `build.gradle`) and compile the project.

3.  **Run the Application:**
    After a successful build, you can run the Spring Boot application using the following Gradle command:
    ```bash
    gradle bootRun
    ```
    This will start the embedded Tomcat server and deploy your application. You should see output in the console indicating that the application has started. By default, Spring Boot applications run on port `8080`.

## Project Structure

spring-boot-user-demo/

└── src/

├── main/

│   └── java/

│       └── com/example/...

│           ├── MainApplication.java

│           ├── model/

│           │   └── User.java

│           ├── repository/

│           │   ├── FakeRepo.java

│           │   └── FakeRepoInterface.java

│           └── service/

│               ├── UserService.java

│               └── UserServiceImpl.java

└── test/

└── java/

└── com/example/...

└── service/

└── UserServiceTests.java

├── build.gradle

└── README.md



## Deliverables

This project includes the following key files:

* `build.gradle`: Includes the `spring-boot-starter-web` dependency.
* `MainApplication.java`: The main entry point of the Spring Boot application, annotated with `@SpringBootApplication`.
* `User.java`: The model class representing a user with `id`, `name`, and `surname` attributes.
* `FakeRepoInterface.java`: Declares methods: `insertUser(id, name, surname)`, `findUserById(id)`, `deleteUser(id)`.
* `FakeRepo.java`: Implements `FakeRepoInterface` using an in-memory `User` object array to simulate data storage, providing implementations for `insertUser`, `findUserById`, and `deleteUser`.
* `UserService.java`: Interface with `addUser(name, surname)`, `getUser(Id)`, `removeUser(Id)` methods.
* `UserServiceImpl.java`: Implements the `UserService` interface, utilizing dependency injection. It includes logic for `addUser` (calls `insertUser` and prints '[name] added'), `removeUser` (calls `deleteUser` and prints '[name] removed'), and `getUser` (calls `findUserById` and prints 'hello [name]'). **Note:** It does not use the `new` keyword for `FakeRepo` instantiation.
* `UserServiceTests.java`: Unit tests for all three service methods: `addUser`, `removeUser`, and `getUser`.
* `README.md`: This file, providing an overview of the project, how to run it, and technologies used.
* `.git/`: (Implicit) The Git repository, following Gitflow branching and commit standards.
