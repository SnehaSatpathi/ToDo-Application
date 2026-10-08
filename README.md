**Todo App**
A simple Todo Application built using Spring Boot, Spring Data JPA, Thymeleaf, and MySQL.
The project demonstrates how to build a Spring Boot application with database connectivity, JPA entity management, and a web-based interface.

🚀 Technologies Used


Java 23


Spring Boot 3.3.5


Spring Web


Spring Data JPA


Thymeleaf


MySQL


Hibernate


Lombok


Maven

📁 Project Structure
todoapp/
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── app/
│   │   │           └── todoapp/
│   │   │               ├── models/
│   │   │               │   └── Task.java
│   │   │               │
│   │   │               └── TodoappApplication.java
│   │   │
│   │   └── resources/
│   │       ├── templates/
│   │       ├── static/
│   │       └── application.properties
│   │
├── pom.xml
└── README.md

🗄️ Database Configuration
The application uses MySQL as its database.
Current database configuration:

spring.datasource.url=jdbc:mysql://localhost:3306/todo-app
spring.datasource.username=root
spring.datasource.password=${DB_PASSWORD}
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQLDialect
The password is loaded through the DB_PASSWORD environment variable rather than being directly stored in the configuration file.

🗄️ Create the Database
Open MySQL and run:
CREATE DATABASE todoapp;

📌 Task Entity
The application contains a Task entity with the following fields:
Field       	Type          	Description
id	          Long	      Unique task identifier
title	       String         	Task title
completed	   boolean	   Task completion status
The id field is automatically generated using JPA, while Lombok's @Data annotation generates common methods such as getters and setters.

⚙️ Dependencies
The project uses:
spring-boot-starter-web
spring-boot-starter-data-jpa
spring-boot-starter-thymeleaf
mysql-connector-j
lombok
spring-boot-starter-test
These dependencies are already configured in the project's pom.xml

▶️ How to Run the Project
1. Clone the Repository
git clone <your-github-repository-url>

2. Open the Project
Open the project in IntelliJ IDEA or another Java IDE.

3. Configure MySQL
Make sure MySQL is running and create the database:
CREATE DATABASE todoapp;

4. Set Database Password
Set the DB_PASSWORD environment variable with your MySQL password.

For Windows PowerShell:
$env:DB_PASSWORD="your_mysql_password"

5. Build the Project
Using Maven:
mvn clean install

6. Run the application
mvn spring-boot:run
Or run the main Spring Boot application directly from IntelliJ IDEA.

🌐 Application
After starting the application, open:
http://localhost:8080

🎯 Project Purpose
This project was created to practice and demonstrate:
Spring Boot application development
REST/Web application development
MySQL database connectivity
Spring Data JPA
Hibernate ORM
Entity creation
Thymeleaf integration
Maven dependency management
Basic CRUD application architecture



























