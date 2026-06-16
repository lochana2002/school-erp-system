# Software Requirements Specification (SRS)

# School ERP System

Version: 1.0

Prepared By: E.H.L.T. Ehelapitiya

Date: 6/16/2026


# 1. Introduction

## 1.1 Purpose

The School ERP System is a web-based application developed to automate and manage various academic and administrative activities of a school. The system centralizes information related to students, teachers, attendance, examinations, and user management into a single platform.

The purpose of this project is to improve efficiency, reduce paperwork, and provide secure access to school information for different user roles.


## 1.2 Scope

The School ERP System will provide the following functionalities:

* User Authentication and Authorization
* Student Management
* Teacher Management
* Attendance Management
* Examination Management
* Dashboard and Reporting
* Role-Based Access Control

The system will be accessible through a web browser and will support multiple user roles.


## 1.3 Intended Audience

This document is intended for:

* Project Developers
* Software Engineers
* System Administrators
* Academic Supervisors
* Testers


## 1.4 Definitions and Acronyms

| Term  | Description                       |
| ----- | --------------------------------- |
| ERP   | Enterprise Resource Planning      |
| RBAC  | Role-Based Access Control         |
| JWT   | JSON Web Token                    |
| Admin | System Administrator              |
| API   | Application Programming Interface |
| DBMS  | Database Management System        |

# 2. Overall Description

## 2.1 Product Perspective

The School ERP System is a standalone web application consisting of:

Frontend Layer (React)

↓

Backend Layer (Node.js + Express)

↓

Database Layer (PostgreSQL)


## 2.2 Product Functions

The system shall:

* Manage user accounts
* Manage student records
* Manage teacher records
* Record attendance
* Manage examinations and results
* Generate reports
* Control access through user roles


## 2.3 User Classes

### Administrator

Responsibilities:

* Manage users
* Manage students
* Manage teachers
* Generate reports
* Configure system settings

### Teacher

Responsibilities:

* Mark attendance
* Manage examination marks
* View assigned students

### Student

Responsibilities:

* View attendance
* View examination results
* Access personal profile



## 2.4 Operating Environment

### Frontend

* React.js
* Tailwind CSS

### Backend

* Node.js
* Express.js

### Database

* PostgreSQL

### Browser Support

* Google Chrome
* Microsoft Edge
* Mozilla Firefox

# 3. System Features

## 3.1 Authentication Module

### Description

Provides secure login and access control.

### Functional Requirements

FR-01 User shall login using email and password.

FR-02 System shall validate user credentials.

FR-03 System shall generate JWT tokens.

FR-04 User shall logout securely.

FR-05 Passwords shall be encrypted before storage.


## 3.2 User Management Module

### Description

Allows administrators to manage system users.

### Functional Requirements

FR-06 Admin shall create users.

FR-07 Admin shall update user information.

FR-08 Admin shall delete users.

FR-09 Admin shall assign roles.

FR-10 Admin shall view all users.

## 3.3 Student Management Module

### Description

Manages student records.

### Functional Requirements

FR-11 Admin shall add students.

FR-12 Admin shall update student details.

FR-13 Admin shall delete students.

FR-14 Admin shall search students.

FR-15 Admin shall view student profiles.

## 3.4 Teacher Management Module

### Description

Manages teacher information.

### Functional Requirements

FR-16 Admin shall add teachers.

FR-17 Admin shall update teacher details.

FR-18 Admin shall delete teachers.

FR-19 Admin shall assign subjects.

FR-20 Admin shall view teacher profiles.

## 3.5 Attendance Management Module

### Description

Records student attendance.

### Functional Requirements

FR-21 Teacher shall mark attendance.

FR-22 Teacher shall edit attendance.

FR-23 Student shall view attendance records.

FR-24 Admin shall generate attendance reports.


## 3.6 Examination Management Module

### Description

Handles examinations and results.

### Functional Requirements

FR-25 Admin shall create examinations.

FR-26 Teacher shall enter marks.

FR-27 System shall calculate total marks.

FR-28 System shall calculate grades.

FR-29 Students shall view results.


## 3.7 Dashboard Module

### Description

Provides analytical information.

### Functional Requirements

FR-30 System shall display total students.

FR-31 System shall display total teachers.

FR-32 System shall display attendance statistics.

FR-33 System shall display examination statistics.


# 4. External Interface Requirements

## 4.1 User Interface

The system shall provide:

* Responsive design
* Dashboard view
* Navigation menu
* Forms for CRUD operations
* Search functionality


## 4.2 Software Interfaces

The system shall integrate with:

* PostgreSQL Database
* REST APIs
* JWT Authentication Service

# 5. Database Requirements

## Main Entities

### Roles

* id
* role_name

### Users

* id
* name
* email
* password
* role_id

### Students

* id
* user_id
* admission_no
* grade
* contact_no

### Teachers

* id
* user_id
* subject
* qualification

### Attendance

* id
* student_id
* date
* status

### Exams

* id
* exam_name
* date

### Results

* id
* student_id
* exam_id
* marks
* grade


# 6. Non-Functional Requirements

## Security

* JWT authentication
* Password hashing using bcrypt
* Role-based authorization
* Secure API endpoints

## Performance

* Average response time below 3 seconds
* Efficient database queries

## Reliability

* System uptime above 99%

## Maintainability

* Modular architecture
* Clean code practices
* Documentation availability

## Scalability

* Support future modules
* Support increased user load

## Availability

* Accessible through internet connection
* Available 24/7


# 7. Constraints

* PostgreSQL must be used as database.
* React must be used for frontend.
* Node.js and Express must be used for backend.
* RESTful APIs shall be implemented.
* JWT authentication shall be used.

# 8. Assumptions and Dependencies

* Users possess internet connectivity.
* Modern browsers are available.
* PostgreSQL server is operational.
* Authentication server is configured correctly.


# 9. Future Enhancements

* Parent Portal
* Online Fee Management
* SMS Notifications
* Email Notifications
* Mobile Application
* AI-Based Academic Analytics
* Timetable Management
* Library Management


# 10. Conclusion

The School ERP System aims to streamline school operations by providing a centralized platform for managing students, teachers, attendance, examinations, and administrative functions. The system will improve efficiency, security, and accessibility while providing a scalable foundation for future enhancements.
