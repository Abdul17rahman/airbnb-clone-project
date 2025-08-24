# 🏠 AirBnb Clone Overview

This project aims to mimic the [AirBnb](https://www.airbnb.com/) application that allows users book apartments and places to stay with the covenience of their phones. The aim is to implement features like bookings, reservation, payments, user profile, authentication. This backend will support various functionalities required to mimic the core features of Airbnb, ensuring a smooth experience for users and hosts.

## 🎯 Project Initialization

- Repository: **airbnb-clone-project**
- Steps:
  1. Create a new public GitHub repo named `airbnb-clone-project`.
  2. Initialize with a `README.md` (this file).
  3. Commit and push changes to GitHub.

## 👨🏼‍💻 Team Roles

According to the project requirements, we shall have 3 different roles and they include:

| Role                    | Responsibilities                                         |
| ----------------------- | -------------------------------------------------------- |
| **Project Manager**     | Oversees development progress, ensures deadlines are met |
| **Frontend Developers** | Build UI in React, integrate APIs, ensure responsiveness |
| **Backend Developers**  | Develop Django REST/GraphQL APIs, manage business logic  |
| **Designers (UI/UX)**   | Create wireframes, Figma mockups, and style guides       |
| **QA/Testers**          | Write and run test cases, ensure bug-free releases       |
| **DevOps Engineers**    | Handle CI/CD, deployment, scaling, monitoring            |
| **Product Owner**       | Defines requirements, prioritizes backlog                |
| **Scrum Master**        | Facilitates agile processes, resolves blockers           |

## ⚙️ Technology Stack

### Backend

- **Django**: A high-level Python web framework used for building the RESTful API.

- **Django Rest Framework**: Provides tools for creating and managing RESTful APIs.

- **PostgreSQL**: A powerful relational database used for data storage.

- **GraphQL**: Allows for flexible and efficient querying of data.

- **Calery**: For handling asynchronous tasks such as sending notifications or processing payments.

- **Redis**: Used for caching and session management.

- **Docker**: Containerization tool for consistent development and deployment environments.

- **CI/CD Pipelines**: Automated pipelines for testing and deploying code changes.

### Frontend

- **React.js** – Core frontend library
- **Next.js** – For SSR (optional, if needed for SEO & performance)
- **Tailwind CSS** – Styling & responsive design
- **Figma** – UI/UX design tool
- **Axios / React Query** – API calls & state management
- **Vercel / Netlify** – Hosting for frontend

## 🎨 UI/UX Design Planning

The design will follow **Airbnb’s minimal, clean, and user-friendly approach** with emphasis on **simplicity, discoverability, and trust**.

### Design Goals

- Intuitive navigation for users
- Clear property listings with images
- Smooth booking flow
- Mobile-first responsive design

### Key Pages

| Page                      | Description                                                               |
| ------------------------- | ------------------------------------------------------------------------- |
| **Property Listing View** | Displays all available properties with filters (price, location, ratings) |
| **Listing Detailed View** | Shows property images, description, reviews, and booking option           |
| **Simple Checkout View**  | Guides users through payment and confirmation of booking                  |

**Why user-friendly design matters?**  
A booking system needs to be **fast, reliable, and easy to use** to avoid user drop-off. A clean interface builds **trust** and ensures users can complete bookings without confusion.

## 🧩 UI Component Patterns

Reusable components will speed up frontend development. Planned components include:

- **Navbar**: Navigation with logo, search, login/profile
- **Property Card**: Displays property image, name, price, rating
- **Footer**: Contains links to help, terms, and social media
- **Booking Form**: Date picker, guest selector, booking button
- **Review Component**: Star ratings, text reviews
- \*\*F

## 🎨 More UI/UX Design Planning (Figma Exploration)

- **Colors**:

  - Primary: `#FF385C` (Airbnb pink/red)
  - Secondary: `#008489` (teal)
  - Background: `#F7F7F7`
  - Text: `#222222`

- **Typography**:
  - Font Family: `Circular Std` (or fallback: Arial, sans-serif)
  - Headings: Bold, 24px+
  - Subheadings: Medium, 18–20px
  - Body: Regular, 14–16px

**Why define design properties?**  
By setting **color styles and typography upfront**, we maintain **consistency**, speed up collaboration, and make the UI **scalable** as new features are added.

## 📉 Database Design

PostgreSQL provides a powerfull database schema that will enable fast data retrieval, query optmization and many other database features. Below is a brief overview of the database design.

### Entities

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

## 📈 API Security

Application security is very important for any project as it enables authentication and authorization. With this implementation users will be able to sign and access their own information, the application sensitive data will as well not access or open for anyone to access as this could lead to attacks.

Weak security mechanisms make an application vulnerable to attacks of all sorts giving hackers access to sensitive application data. This application will have the following api security features.

- **Authentication**: This is a process of verying who the signed/logged in user is. It helps making sure only authorized users can access certain features or data — like your properties, bookings, or user profile.

- **Authorisation**: This is a process of determining weather an authenticated user has the right access to specific application resources or features. Even if a user logs in successfully, they shouldn't be able to do everything.

- **Rate Limiting**: This technique allows APIs manage requests by limiting how many requests a user can make to the API in a specific period of time. It helps protect an API from **Abuse** spamming login attemps, **DDOS attacks** flooding the server with fake requests from bots, **Server overload** too many user requests at once and many others.

## ⳽ CI/CD Pipeline

Continous intergration, Continous Deployment/Delivery is a practice that automates building, testing, and deploying code so that software changes can be delivered quickly, reliably, and continuously. These 2 are a crucial part of application production as they enable updates without breaking the operations of the application. Changes are committed to live production application and it's enabled with tools such as:

- **Docker**: This enables running a virtual application enviroment that includes all the tools an application needs to run smoothly without issues. Applications are packaged into lightweight, portable containers that run consistently accross different enviroments.

- **GitHub Actions**: This is a pipeline platform that leverages github to automate testing, building and deployment of applications through events like pushes or pull requests in a repository.

> This document was done and updated by Abdul Rahman.
