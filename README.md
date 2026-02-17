Smart EV Charging Management Platform — User Microservice

This project is part of a microservices-based Smart EV Charging Management System developed using Spring Boot and MySQL. The system is designed to simulate a real-world EV charging infrastructure where users can register, manage accounts, and interact with charging services.

Project Overview

The User Service is responsible for:

* User registration
* Retrieving user details
* Managing user data in a database

This microservice will later integrate with WSO2 API Manager, WSO2 Identity Server, and other microservices such as Charging Station Service and Booking Service.

Technology Stack

* Java
* Spring Boot
* Spring Data JPA (Hibernate)
* MySQL
* Maven
* REST API
* Postman for testing

Project Structure

src/main/java/com/ev/user_service

* controller — REST controllers
* service — Business logic
* repository — Database access layer
* entity — JPA entities
* UserServiceApplication.java — Main application

API Endpoints

Create User

POST /users

Example Request

{
"name": "Vinod",
"email": "[vinod@gmail.com](mailto:vinod@gmail.com)",
"password": "1234"
}

Get All Users

GET /users

Database Configuration

Database name: ev_users

Configured in application.properties:

spring.datasource.url=jdbc:mysql://localhost:3306/ev_users
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD

How to Run

Using Maven Wrapper:

./mvnw spring-boot:run

Application runs on:

http://localhost:8081

Future Improvements

* Integration with WSO2 API Manager
* Authentication using WSO2 Identity Server
* Docker containerization
* Additional microservices (Station, Booking, Payment)

Author

Vinod Perera
GitHub: https://github.com/Perera1325
