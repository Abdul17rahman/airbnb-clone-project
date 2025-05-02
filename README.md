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

## Database Design

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
