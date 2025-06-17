# Airbnb Clone Project

## Overview

The Airbnb Clone Project is a comprehensive backend-focused simulation of the Airbnb platform. It is designed to help learners build real-world experience in full-stack development with a strong emphasis on backend architecture, database design, API security, and DevOps practices.

This project includes collaborative GitHub workflows, secure API development with Django, relational database modeling using PostgreSQL, and efficient CI/CD pipeline management using GitHub Actions and Docker.

---

## Team Roles

- **Backend Developer**: Responsible for building the application logic, developing RESTful APIs, and ensuring integration with the frontend.
- **Database Administrator**: Designs and manages the database schema, ensures data integrity, and handles migrations and optimizations.
- **DevOps Engineer**: Sets up Docker environments, manages GitHub Actions for CI/CD, and ensures smooth deployment workflows.
- **Security Engineer**: Implements API authentication, access control, encryption, and monitors for vulnerabilities.
- **Project Manager**: Oversees project timelines, coordinates tasks among team members, and ensures documentation is complete.

---

## Technology Stack

- **Django**: Python-based web framework used for building scalable and secure REST APIs.
- **PostgreSQL**: A powerful open-source relational database system used to store and query application data.
- **GraphQL**: An API query language allowing clients to request exactly what they need, improving flexibility and performance.
- **Docker**: Containerization platform for running the application in consistent environments across development and production.
- **GitHub Actions**: CI/CD tool for automating build, test, and deployment workflows.

---

## Database Design

### Key Entities

1. **User**
   - `id`
   - `name`
   - `email`
   - `password_hash`
   - `host` (Boolean)

2. **Property**
   - `id`
   - `owner_id` (FK to User)
   - `title`
   - `location`
   - `price_per_night`

3. **Booking**
   - `id`
   - `user_id` (FK to User)
   - `property_id` (FK to Property)
   - `start_date`
   - `end_date`

4. **Review**
   - `id`
   - `booking_id` (FK to Booking)
   - `rating`
   - `comment`

5. **Payment**
   - `id`
   - `booking_id` (FK to Booking)
   - `amount`
   - `payment_status`

### Relationships

- A **User** can list multiple **Properties**.
- A **Booking** is made by a **User** for a **Property**.
- Each **Booking** may have one **Review** and one **Payment**.
- **Payments** are linked to bookings and track payment status.

---

## Feature Breakdown

- **User Management**: Users can register, log in, update profiles, and manage roles (guest/host).
- **Property Management**: Hosts can list, update, and delete property listings with descriptions, prices, and availability.
- **Booking System**: Users can book available properties for specific dates and manage existing bookings.
- **Review System**: After completing a stay, users can submit ratings and reviews for the properties they booked.
- **Payment Integration**: Secure payment processing for bookings, including tracking of transaction status and refunds.

---

## API Security

- **Authentication**: JSON Web Token-based authentication ensures users are securely logged in and sessions are managed appropriately.
- **Authorization**: Role-based access control ensures users can only access permitted resources (e.g., only hosts can edit their listings).
- **Rate Limiting**: Protects the API from brute-force attacks and abuse by limiting repeated requests from clients.
- **Input Validation**: Ensures that all incoming data is clean and secure to prevent common vulnerabilities like SQL Injection.

### Importance of Security

- Protects sensitive user data including personal details and payment info.
- Ensures trust and reliability for users interacting with the system.
- Prevents unauthorized access and potential misuse of the platform.

---

## CI/CD Pipeline

CI/CD (Continuous Integration and Continuous Deployment) helps automate the process of testing, building, and deploying software.

### Tools Used

- **GitHub Actions**: Automates testing and deployment processes with triggers on push, PRs, or releases.
- **Docker**: Ensures consistent development and production environments using containerized services.
- **PostgreSQL Service**: Used for integration testing during CI stages.

### Benefits

- Improves team productivity and code quality.
- Detects bugs early through automated tests.
- Enables faster, reliable deployments and rollback support.

---

## License

This project is for educational purposes only and does not claim any affiliation with Airbnb.

---

## Authors

- Warega Moses and Team that is Backend Engineers, ProDev Learners, and Security Enthusiasts.
