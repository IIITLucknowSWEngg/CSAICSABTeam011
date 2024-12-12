# Design Document for Myntra 2.0

## Table of Contents
1. [Overview](#overview)  
2. [System Architecture](#system-architecture)  
3. [Design Principles](#design-principles)  
4. [Data Flow](#data-flow)  
5. [User Interface Design](#user-interface-design)  
6. [API Design](#api-design)  
7. [Database Design](#database-design)  

---

## 1. Overview
Myntra 2.0 is a next-generation e-commerce platform for fashion and lifestyle products. The platform is built to provide a seamless user experience, ensuring scalability, performance, and security. The system is developed using a **microservices architecture** with a responsive, user-friendly **frontend**. It supports essential features like user authentication, product browsing, cart management, order processing, and payment integration.

---

## 2. System Architecture
The system follows a **microservices-based architecture** for flexibility, maintainability, and scalability. Below is a high-level view of the architecture:

2.1 **Frontend**
- **Technologies**: ReactJS, Redux, TailwindCSS, Axios
- **Role**: Handles user interaction, provides dynamic and responsive web pages, and communicates with the backend via REST APIs.

2.2 **Backend**
- **Technologies**: Node.js, FastAPI (Python), Docker, Kubernetes
- **Microservices**:
  - **User Service**: Manages user authentication and profile data.
  - **Product Service**: Manages product catalog, filters, and categories.
  - **Order Service**: Handles cart, checkout, payments, and order tracking.
  - **Recommendation Service**: Provides AI-based product recommendations.
  - **Notification Service**: Sends email, SMS, and app notifications.

2.3 **Databases**
- **PostgreSQL**: For relational data (users, orders, payments, etc.).  
- **MongoDB**: For product catalog, product details, and inventory.  
- **Redis**: For caching frequently accessed data like user sessions and cart details.  

2.4 **Deployment**
- **Containerization**: Docker for containerizing services.  
- **Orchestration**: Kubernetes for scaling and managing containers.  
- **Cloud Provider**: AWS (Amazon Web Services) for hosting.  

---

## 3. Design Principles
The following principles guide the development and design of Myntra 2.0:

- **Modularity**: Independent services for better maintainability.  
- **Scalability**: Horizontal scaling through container orchestration (Kubernetes).  
- **Security**: Role-based access control (RBAC), secure payment handling, and encrypted user data.  
- **Performance**: Use of Redis caching, load balancers, and optimized database queries.  
- **Responsiveness**: A mobile-first approach for a smooth, fast experience on all devices.  

---

## 4. Data Flow
This section outlines how data flows within the system:

1. **User Request**: A user initiates a request from the UI (e.g., viewing a product).  
2. **API Gateway**: The request is routed through the API Gateway, which directs it to the appropriate service.  
3. **Microservices**: The specific microservice (e.g., Product Service) processes the request.  
4. **Database**: The service interacts with the database (PostgreSQL or MongoDB) to retrieve or update information.  
5. **Response**: The microservice sends a response back through the API Gateway to the user.  

---

## 5. User Interface Design
The UI follows a **mobile-first approach** to ensure a seamless user experience across devices. Below are the main pages and their components:

### **1. Homepage**
- **Header**: Search bar, category navigation, and login/cart icons.  
- **Product Grid**: List of products with images, prices, and "Add to Cart" buttons.  
- **Footer**: Links to terms, privacy policy, and support.  

### **2. Product Detail Page**
- **Image Gallery**: Shows multiple views of the product.  
- **Product Info**: Name, price, size, color, and availability.  
- **Add to Cart**: Button to add the product to the cart.  

### **3. Cart/Checkout Page**
- **Product List**: Items in the cart with options to edit quantity or remove.  
- **Order Summary**: Total cost, taxes, and delivery charges.  
- **Payment Gateway**: Options to pay via UPI, card, or wallet.  

---

## 6. API Design
APIs enable the frontend to communicate with the backend microservices. Here are some key endpoints:

### **User Service**
| **Endpoint** | **Method** | **Description** |
|--------------|------------|------------------|
| `/api/user/register` | POST | Register a new user. |
| `/api/user/login` | POST | Log in an existing user. |
| `/api/user/profile` | GET | Get user profile details. |

### **Product Service**
| **Endpoint** | **Method** | **Description** |
|--------------|------------|------------------|
| `/api/products` | GET | Fetch all products. |
| `/api/products/{id}` | GET | Get product details by ID. |
| `/api/products/search` | GET | Search for products by name, category, or filters. |

### **Order Service**
| **Endpoint** | **Method** | **Description** |
|--------------|------------|------------------|
| `/api/cart` | GET | Get the current cart. |
| `/api/cart/add` | POST | Add a product to the cart. |
| `/api/cart/remove` | POST | Remove a product from the cart. |
| `/api/order` | POST | Place an order. |

---

## 7. Database Design
The following schema highlights the key database tables and collections.

### **1. PostgreSQL**
- **Users Table**  
  | **Field**      | **Data Type** | **Description**         |
  |----------------|---------------|-------------------------|
  | `user_id`      | INT (PK)      | Unique identifier for each user. |
  | `email`        | VARCHAR(255)  | User's email address.  |
  | `password`     | VARCHAR(255)  | Hashed user password.   |
  | `role`         | ENUM('admin', 'user') | Role of the user.     |

- **Orders Table**  
  | **Field**      | **Data Type** | **Description**         |
  |----------------|---------------|-------------------------|
  | `order_id`     | INT (PK)      | Unique identifier for each order. |
  | `user_id`      | INT (FK)      | Reference to the user who placed the order. |
  | `total_price`  | DECIMAL(10,2) | Total cost of the order. |
  | `status`       | ENUM('pending', 'shipped', 'delivered') | Order status.  |

### **2. MongoDB**
- **Products Collection**  
  ```json
  {
    "product_id": "P123",
    "name": "Men's T-shirt",
    "description": "100% cotton t-shirt",
    "price": 999.99,
    "stock": 50,
    "category": "Men's Wear"
  }
