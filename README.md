# Student Course Management System

A RESTful web application developed using Java and Spring Boot for managing student records. The application provides CRUD operations, search functionality, pagination, input validation, exception handling, and MySQL database integration.

## Project Overview

The Student Course Management System is designed to simplify the management of student information through REST APIs.

The application follows a layered architecture using:

- Controller Layer
- Service Layer
- Repository Layer
- Model Layer
- Exception Handling Layer

The application uses Spring Data JPA for database operations and MySQL for persistent data storage.

## Features

- Add a new student
- View all students
- View student details by ID
- Update student information
- Delete student records
- Search students by city
- Search students by course
- Pagination for student records
- Input validation
- Global exception handling
- MySQL database integration
- RESTful API architecture

## Technologies Used

| Technology | Purpose |
|------------|---------|
| Java 17 | Application development |
| Spring Boot | Backend application framework |
| Spring Web | REST API development |
| Spring Data JPA | Database interaction |
| MySQL | Relational database |
| Maven | Build and dependency management |
| Jakarta Validation | Input validation |
| Lombok | Reducing boilerplate code |
| Postman | API testing |
| Git & GitHub | Version control |

## Project Structure

```text
StudentManagementSystem
│
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com
│   │   │       └── shaista
│   │   │           └── studentmanagement
│   │   │               │
│   │   │               ├── StudentManagementApplication.java
│   │   │               │
│   │   │               ├── controller
│   │   │               │   └── StudentController.java
│   │   │               │
│   │   │               ├── service
│   │   │               │   └── StudentService.java
│   │   │               │
│   │   │               ├── repository
│   │   │               │   └── StudentRepository.java
│   │   │               │
│   │   │               ├── model
│   │   │               │   └── Student.java
│   │   │               │
│   │   │               └── exception
│   │   │                   ├── StudentNotFoundException.java
│   │   │                   ├── ErrorResponse.java
│   │   │                   └── GlobalExceptionHandler.java
│   │   │
│   │   └── resources
│   │       └── application.properties
│   │
│   └── test
│       └── java
│           └── com
│               └── shaista
│                   └── studentmanagement
│                       └── StudentManagementApplicationTests.java
│
├── .gitignore
├── mvnw
├── mvnw.cmd
├── pom.xml
└── README.md
```
Application Architecture
The application follows a layered architecture:
```text
Client / Postman
       |
       v
Controller
       |
       v
Service
       |
       v
Repository
       |
       v
MySQL Database
```
## Controller Layer
Handles HTTP requests and exposes REST API endpoints.
## Service Layer
Contains the application logic and coordinates operations between the controller and repository.
## Repository Layer
Uses Spring Data JPA to perform database operations.
## Model Layer
Defines the student entity and its database representation.
## Exception Layer
Handles application errors and provides structured error responses.
## Database Configuration
Create a MySQL database:
CREATE DATABASE studentdb;

Configure the database connection in:
src/main/resources/application.properties

Example:
```java
spring.datasource.url=jdbc:mysql://localhost:3306/studentdb
spring.datasource.username=root
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```
Replace your_password with your local MySQL password.
REST API Endpoints
```
Method	Endpoint	Description
GET	/students	Retrieve all students
GET	/students/{id}	Retrieve a student by ID
POST	/students	Add a new student
PUT	/students/{id}	Update student details
DELETE	/students/{id}	Delete a student
GET	/students/city/{city}	Search students by city
GET	/students/course/{course}	Search students by course
GET	/students/page?page=0&size=5	Retrieve students using pagination
```

Sample API Request
Add Student
POST
http://localhost:8080/students

Request body:
{
    "name": "Ananya Sharma",
    "age": 21,
    "course": "Computer Science",
    "city": "Chennai"
}

Get All Students
GET
http://localhost:8080/students

Get Student by ID
GET
http://localhost:8080/students/1

Update Student
PUT
http://localhost:8080/students/1

Delete Student
DELETE
http://localhost:8080/students/1

How to Run the Project
Prerequisites
Make sure the following are installed:
- Java 17 or later
- MySQL
- Maven or Maven Wrapper
- Postman
- Git
Steps
1. Clone the repository
git clone https://github.com/YOUR_USERNAME/student-course-management-system.git

2. Open the project
Open the project using IntelliJ IDEA, Eclipse, Spring Tool Suite, or VS Code.
3. Configure MySQL
Create the database:
CREATE DATABASE studentdb;

Update the MySQL username and password in:
src/main/resources/application.properties

4. Build the project
Using Maven Wrapper:
.\mvnw.cmd clean install

5. Run the application
.\mvnw.cmd spring-boot:run

The application will start on:
http://localhost:8080

6. Test the APIs
Use Postman to send requests to the available REST endpoints.
Testing
The project includes Spring Boot test support for verifying application functionality.
Run the tests using:
.\mvnw.cmd test

The test configuration verifies that the Spring application context loads successfully.
Error Handling
The application includes centralized exception handling for cases such as requesting a student record that does not exist.
The exception handling structure includes:
StudentNotFoundException
ErrorResponse
GlobalExceptionHandler

This helps provide consistent error responses from the REST API.
Learning Outcomes
Through this project, I gained practical experience in:
- Java application development
- Spring Boot
- REST API development
- Object-Oriented Programming
- Spring Data JPA
- MySQL database integration
- CRUD operations
- Input validation
- Exception handling
- Pagination
- Maven project management
- API testing with Postman
- Git and GitHub
- Layered application architecture
Future Enhancements
Possible improvements for future versions include:
- Spring Security authentication
- JWT-based authentication
- Role-based access control
- Swagger/OpenAPI documentation
- Sorting and advanced filtering
- Docker containerization
- Additional unit and integration tests
Author
Shaista Mulla
B.Tech Computer Science and Engineering (AI & ML)
Rajeev Gandhi Memorial College of Engineering and Technology (RGMCET), JNTUA
Connect with Me
- LinkedIn: https://www.linkedin.com/in/shaista-mulla-505741280/
- GitHub: https://github.com/Shaie1383/
- Portfolio: https://portfolio-shaista.netlify.app/
License
This project is developed for learning and academic purposes.

update the README so it accurately reflects **your modified version**, and we can make the GitHub repository look like a proper fresher Java project.
