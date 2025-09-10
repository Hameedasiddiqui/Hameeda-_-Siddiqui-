
Student Manager Project

Introduction
The Student Manager project is a full-stack application that helps manage student information (e.g., name, email, course, enrollment details). It is built using:

Spring Boot REST API (Backend)

Angular (Frontend UI)

PostgreSQL (Database)

The system provides functionalities like add student, view students, update student details, and delete student records.

Architecture
This project follows MVC architecture and 3-tier design:

Frontend (Angular – View Layer)
Provides an intuitive UI for managing students.

Uses Angular components, services, and routing.

Calls backend APIs via Angular HttpClient.

Built with HTML, CSS, Bootstrap for responsive design.

Backend (Spring Boot – Controller & Service Layer)
Controllers → Expose REST API endpoints (/students).

Services → Contain business logic for student management.

Repositories (Spring Data JPA) → Handle database operations.

JSON data is exchanged with Angular frontend.

Database (PostgreSQL – Model Layer)
Stores student records.

Connected via Spring Data JPA + Hibernate.

Table Example:

CREATE TABLE students ( id SERIAL PRIMARY KEY, name VARCHAR(100) NOT NULL, email VARCHAR(100) UNIQUE NOT NULL, course VARCHAR(100), enrollment_date DATE );

Workflow

User interacts with Angular UI (e.g., clicks "Add Student").

Angular sends an HTTP POST request to Spring Boot REST API.

Spring Boot Controller receives the request and calls the Service layer.

Service layer validates input and interacts with Repository.

Repository saves/reads data from PostgreSQL.

JSON response is returned to Angular.

Angular updates the UI dynamically (student list, forms, etc.).

Features

➕ Add Student – Register a new student.

📋 View Students – Display all students in a responsive table.

✏ Update Student – Modify existing student details.

❌ Delete Student – Remove student records.

🔎 Search/Filter – Search students by name or course.

Technologies Used
Backend → Spring Boot, REST API, Spring Data JPA, Hibernate

Database → PostgreSQL

Frontend → Angular, TypeScript, HTML5, CSS3, Bootstrap

Tools → Postman, pgAdmin, IntelliJ IDEA, VS Code

Advantages
✅ Simple and intuitive student management system. ✅ Clear separation of concerns (MVC). ✅ Responsive UI with Angular + Bootstrap. ✅ REST APIs → reusable for mobile or other frontends. ✅ PostgreSQL → robust and reliable storage.

Disadvantages / Challenges
⚠ Initial setup of Angular + Spring Boot can be complex. ⚠ Requires handling CORS for API communication. ⚠ PostgreSQL setup needed on local/remote environment.

Conclusion
The Student Manager Project is a full-stack solution for managing student data effectively. It demonstrates proper integration of Angular frontend with Spring Boot backend and PostgreSQL database using MVC architecture. This project can be extended to include authentication, role-based access, dashboards, and reports for real-world use.