# 🏠 AirBnb Clone Overview

This project aims to mimic the [AirBnb](https://www.airbnb.com/) application that allows users book apartments and places to stay with the covenience of their phones. The aim is to implement features like bookings, reservation, payments, user profile, authentication. This backend will support various functionalities required to mimic the core features of Airbnb, ensuring a smooth experience for users and hosts.

## 👨🏼‍💻 Team Roles

According to the project requirements, we shall have 3 different roles and they include:

- **Backend Developer**: Responsible for implementing API endpoints, database schemas, and business logic.

- **Database Addministrator**: Manages database design, indexing, and optimizations.

- **DevOps Engineer**: Handles deployment, monitoring, and scaling of the backend services.

- **QA Enginner**: Ensures the backend functionalities are thoroughly tested and meet quality standards.

## ⚙️ Technology Stack

- **Django**: A high-level Python web framework used for building the RESTful API.

- **Django Rest Framework**: Provides tools for creating and managing RESTful APIs.

- **PostgreSQL**: A powerful relational database used for data storage.

- **GraphQL**: Allows for flexible and efficient querying of data.

- **Calery**: For handling asynchronous tasks such as sending notifications or processing payments.

- **Redis**: Used for caching and session management.

- **Docker**: Containerization tool for consistent development and deployment environments.

- **CI/CD Pipelines**: Automated pipelines for testing and deploying code changes.

## 📉 Database Design

PostgreSQL provides a powerfull database schema that will enable fast data retrieval, query optmization and many other database features. Below is a brief overview of the database design.

### Entries

- **Users**: Each user can have multiple bookings and will have different fields including:

  - username
  - password
  - email

- **Bookings**: Each booking will belong to one specific user and one property. It will have fields including:

  - booking_id
  - user_id
  - property_id
  - booking_date

- **Properties**: Each property will belong to one owner and will have a single booking at a time. Fields include among others:

  - property_id
  - owner_id
  - status

- **Payments**: Each payment will belong to a spefic booking and will have fields including.
  - payment_id
  - booking_id

## 🛠️ Feature Breakdown

The application will have different features including but not limited.

### 1. User Management

The application will have a secure system for user registration, authentication, and profile management.

Users will be able to signup, login and logout efficiently without any hustle.

### 2. Booking System

The application will have a booking mechanism for users to reserve properties and manage booking details.

The Booking system will be liked to properties, users and payments.

### 3. Review System

This will allow users to leave reviews and ratings for properties.

It will as well enables users checkout reviews of different properties before they book them for better decision making.

## API Security

Application security is very important for any project as it enables authentication and authorization. With this implementation users will be able to sign and access their own information, the application sensitive data will as well not access or open for anyone to access as this could lead to attacks.

Weak security mechanisms make an application vulnerable to attacks of all sorts giving hackers access to sensitive application data. This application will have the following api security features.

- **Authentication**: This is a process of verying who the signed/logged in user is. It helps making sure only authorized users can access certain features or data — like your properties, bookings, or user profile.

- **Authorisation**: This is a process of determining weather an authenticated user has the right access to specific application resources or features. Even if a user logs in successfully, they shouldn't be able to do everything.

- **Rate Limiting**: This technique allows APIs manage requests by limiting how many requests a user can make to the API in a specific period of time. It helps protect an API from **Abuse** spamming login attemps, **DDOS attacks** flooding the server with fake requests from bots, **Server overload** too many user requests at once and many others.
