# airbnb-clone-project

## 📌 Project Overview

This project is an Airbnb Clone built using Django and PostgreSQL. It allows users to list, browse, and book properties online, providing a seamless platform for hosts and guests.

## 🎯 Project Goals

- Learn real-world backend architecture and design patterns  
- Practice secure API development and user authentication  
- Implement CI/CD pipelines for scalable and reliable deployment  

## 🧑‍🤝‍🧑 Team Roles

### 👨‍💻 Backend Developer  
Responsible for implementing API endpoints, designing database schemas, and developing business logic to power the platform.

### 🗄️ Database Administrator  
Manages database design, indexing, and performance optimization to ensure data integrity and efficiency.

### 🚀 DevOps Engineer  
Handles deployment, monitoring, scaling, and automation of backend services for smooth production operations.

### 🧪 QA Engineer  
Ensures backend functionalities are thoroughly tested, performs automated and manual testing to maintain quality standards.

## 💻 Technology Stack

### 🐍 Django  
A high-level Python web framework used for building the RESTful API, providing rapid development and clean design.

### 🚀 Django REST Framework  
Extends Django to simplify creating RESTful APIs, enabling efficient serialization and request handling.

### 🐘 PostgreSQL  
A powerful open-source relational database for reliable and scalable data storage.

### 🔎 GraphQL  
Provides flexible and efficient querying of data, allowing clients to request exactly what they need.

### 🎯 Celery  
Handles asynchronous tasks like sending notifications and processing payments, improving responsiveness.

### 🧠 Redis  
Used as an in-memory data store for caching and session management to speed up the application.

### 🐳 Docker  
Containerizes the application for consistent development and deployment environments across machines.

### 🔁 CI/CD Pipelines  
Automates testing, building, and deployment workflows to improve code quality and delivery speed.

## 🗂️ Database Design

### 🧩 Entities

#### User  
- `id`: Unique identifier for each user  
- `name`: Full name of the user  
- `email`: Email address used for login and communication  
- `password`: Hashed password for authentication  
- `role`: User role (guest, host, admin)

#### Property  
- `id`: Unique property identifier  
- `title`: Name or title of the property listing  
- `location`: Geographical location of the property  
- `price`: Price per night or stay period  
- `user_id`: Reference to the owning user (host)

#### Booking  
- `id`: Unique booking identifier  
- `user_id`: Reference to the guest who made the booking  
- `property_id`: Reference to the booked property  
- `start_date`: Booking start date  
- `end_date`: Booking end date  
- `status`: Booking status (confirmed, cancelled, pending)

#### Review  
- `id`: Unique review identifier  
- `user_id`: Reference to the user who wrote the review  
- `property_id`: Reference to the reviewed property  
- `rating`: Numeric rating value  
- `comment`: Text feedback  
- `created_at`: Timestamp of when the review was created

#### Payment  
- `id`: Unique payment identifier  
- `booking_id`: Reference to the associated booking  
- `amount`: Payment amount  
- `payment_method`: Method used (credit card, PayPal, etc.)  
- `status`: Payment status (paid, refunded, failed)  
- `paid_at`: Timestamp of payment completion

### 🔑 Relationships

- A **User** can own multiple **Properties** (One-to-Many).  
- A **Booking** belongs to one **Property** and one **User** (Many-to-One).  
- A **User** can leave multiple **Reviews** for different **Properties**.  
- Each **Review** is linked to one **User** and one **Property**.  
- Each **Payment** is associated with one **Booking**.

## ✨ Feature Breakdown

### 👤 User Management  
Includes user registration, login, email verification, authorization, and session management to ensure secure, personalized experiences.

### 🏠 Property Management  
Allows hosts to list properties with descriptions, prices, availability, and enables updates dynamically.

### 📅 Booking System  
Users can reserve properties, manage booking dates, check status, and receive confirmations, streamlining the reservation workflow.

### ⭐ Rating & Review System  
Guests can rate and review properties post-stay, fostering trust and informed decision-making.

### 💳 Payment Processing  
Secure payments integrated via trusted gateways, supporting real-time transactions, receipts, and refunds.

## 🔐 API Security

### ✅ Authentication  
Implements JWT tokens for secure user identity verification, preventing unauthorized access.

### ✅ Authorization  
Role-based access control ensures users only access permitted features (e.g., guests vs. hosts vs. admins).

### ✅ Rate Limiting  
Limits API requests per user/IP to mitigate abuse and DoS attacks.

### ✅ Data Validation & Sanitization  
All inputs are validated and sanitized to prevent SQL injection, XSS, and other vulnerabilities.

### ✅ HTTPS Enforcement  
All API communication is secured via HTTPS to encrypt data in transit.

### ✅ Secure Payment Handling  
Payments are processed through trusted third-party services; sensitive data is never stored directly.

## ⚙️ CI/CD Pipeline

### 📌 Benefits  
- **Early Bug Detection:** Automated tests run on each code push, preventing regressions.  
- **Fast Feedback Loop:** Immediate alerts on issues speed up fixes.  
- **Reliable Deployment:** Automated builds and deployments reduce human error and ensure consistency.

### 🧰 Tools Used  
- **GitHub Actions:** Automates testing, building, and deployment workflows.  
- **Docker:** Provides consistent environments across development and production.  
- **Cloud Platforms (Heroku, Render, Railway):** Hosts and serves the live application.


