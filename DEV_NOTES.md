# Developer Notes – Expense Tracking System

These notes record the concepts learned, setups completed, and problems solved while building the Expense Tracking System.
They are meant for revision and understanding the development process step by step.

---

## 1. Project Goal

Build a full-stack expense tracking application using:

* Java
* Spring Boot
* PostgreSQL
* Hibernate (JPA)
* Git and GitHub

Purpose:

* Understand backend architecture
* Learn REST API development
* Practice database integration
* Follow real-world project structure

---

## 2. Initial Project Setup

Project folder structure:

expense-tracking-system
├ backend
├ frontend
├ README.md
├ DEV_NOTES.md
└ .gitignore

Backend will contain the Spring Boot application.
Frontend will later contain the React interface.

---

## 3. Technologies Introduced

### Spring Boot

Spring Boot is used to simplify backend development.

Main advantages:

* Auto configuration
* Embedded web server
* Easy dependency management
* Fast application setup

When the application runs it automatically:

1. Starts an embedded Tomcat server
2. Loads application configuration
3. Initializes Spring context
4. Connects to the database

---

### Embedded Tomcat Server

Spring Boot includes Tomcat internally.

This means:

* No need to install Tomcat separately
* The application runs like a standalone server

Application URL:

http://localhost:8080

---

### PostgreSQL Database

PostgreSQL is used as the relational database.

It stores structured data inside tables.

Example structure:

| id | title | amount | category | date |

Each row represents one expense entry.

Useful commands learned:

List databases:

\l

Disable pager:

\pset pager off

Create database:

CREATE DATABASE expense_tracker;

Exit PostgreSQL:

\q

---

### Hibernate / JPA

Hibernate is an ORM tool.

ORM means:

Object Relational Mapping

Mapping:

Java Class → Database Table
Java Object → Row
Java Field → Column

Example:

Expense.java → expense table

This allows developers to interact with the database using Java instead of raw SQL.

---

### Hikari Connection Pool

Spring Boot uses HikariCP for database connection pooling.

Purpose:

Opening a database connection repeatedly is expensive.

Connection pooling allows the application to reuse connections.

Benefits:

* Better performance
* Faster database operations
* Efficient resource usage

---

## 4. Backend Architecture

The backend will follow layered architecture:

Controller → handles HTTP requests
Service → contains business logic
Repository → interacts with database
Model (Entity) → represents database tables

Flow:

Client Request
↓
Controller
↓
Service
↓
Repository
↓
Database

---

## 5. Git and GitHub Setup

Steps performed:

1. Initialized Git repository
2. Connected project to GitHub
3. Created commits for project setup
4. Resolved branch conflicts
5. Added `.gitignore`
6. Removed IDE configuration files

Commands used frequently:

git init
git add .
git commit -m "message"
git push

Repository hosted on GitHub.

---

## 6. Problems Faced and Solutions

### Git branch conflict (main vs master)

Problem:

Local branch was `master` while GitHub used `main`.

Solution:

Renamed local branch to main and reconnected upstream.

---

### Merge conflicts with `.idea` files

Problem:

IDE files created conflicts when merging histories.

Solution:

Added `.gitignore` and removed `.idea` from Git tracking.

---

### Dubious ownership error in Git

Problem:

Git detected repository ownership mismatch.

Solution:

Removed incorrect repository initialization and recreated Git in project folder.

---

## 7. Current Project Status

Completed:

* Spring Boot backend initialized
* PostgreSQL database connected
* Hibernate configured
* Tomcat server running
* GitHub repository created
* Git workflow established

Next development steps:

* Create Expense Entity
* Create Repository layer
* Implement Service layer
* Build REST API endpoints
* Integrate frontend

---

## 8. Key Concepts Learned So Far

* Spring Boot auto configuration
* Embedded web server
* Database connectivity
* Hibernate ORM
* Git version control workflow
* Project structure best practices

---

## 9. Future Learning Topics

While building this project the following concepts will be explored:

* REST API design
* CRUD operations
* DTO and validation
* Authentication and security
* Frontend integration with React
* Docker containerization
* Deployment strategies

---

## Notes

This file will continue to grow as new features and concepts are implemented.
It acts as a personal knowledge log for revisiting concepts learned during development.
