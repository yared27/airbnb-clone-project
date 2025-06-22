# airbnb-clone-project

## 🧑‍🤝‍🧑 Team Roles

### 👨‍💻 Backend Developer  
Responsible for implementing API endpoints, designing database schemas, and developing business logic.

### 🗄️ Database Administrator  
Manages database design, indexing, and performance optimization.

### 🚀 DevOps Engineer  
Handles deployment, monitoring, and scaling of backend services.

### 🧪 QA Engineer  
Ensures backend functionalities are thoroughly tested and meet quality standards.

## 💻 Technology Stack

### 🐍 Django  
A high-level Python web framework used for building the RESTful API.

### 🚀 Django REST Framework  
Provides tools for creating and managing RESTful APIs.

### 🐘 PostgreSQL  
A powerful relational database used for data storage.

### 🔎 GraphQL  
Allows for flexible and efficient querying of data.

### 🎯 Celery  
For handling asynchronous tasks such as sending notifications or processing payments.

### 🧠 Redis  
Used for caching and session management.

### 🐳 Docker  
Containerization tool for consistent development and deployment environments.

### 🔁 CI/CD Pipelines  
Automated pipelines for testing and deploying code changes.

## 🗂️ Database Design

### 🧩 Entities
- **User**
- **Property**
- **Booking**
- **Review**
- **Payment**

### 🔑 Relationships
- A **User** can own multiple **Properties** (One-to-Many).
- A **Booking** belongs to a **Property** and is made by a **User**.
- A **User** can leave multiple **Reviews** for different **Properties**.
- Each **Review** is linked to both a **User** and a **Property**.
- A **Payment** is associated with a specific **Booking**.

### 📌 Key Fields (Examples)
#### User
- `id`, `name`, `email`, `password`, `role`

#### Property
- `id`, `title`, `location`, `price`, `user_id`

#### Booking
- `id`, `user_id`, `property_id`, `start_date`, `end_date`, `status`

#### Review
- `id`, `user_id`, `property_id`, `rating`, `comment`, `created_at`

#### Payment
- `id`, `booking_id`, `amount`, `payment_method`, `status`, `paid_at`
