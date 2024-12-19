# User Requirements Document (URD) for Mynthra 2.0

## 1. Introduction

### 1.1 Purpose
This document outlines the requirements for the Mynthra 2.0 platform. It will guide the design, development, and testing of the platform to ensure it meets the needs of different user roles, including shoppers, vendors, and administrators. The document ensures that the platform provides a seamless shopping experience, efficient vendor management, and robust administrative oversight.

### 1.2 Scope
Mynthra 2.0 will be an e-commerce platform that facilitates online shopping for a wide range of products. The platform allows shoppers to browse products, make purchases, and track orders. Vendors can manage product listings, track sales, and process orders. Administrators oversee platform operations, manage user accounts, and ensure smooth functionality. The scope includes account management, product catalog, shopping cart, order placement, and real-time tracking for all stakeholders.

### 1.3 Definitions, Acronyms, and Abbreviations
- **Shoppers**: Individuals using the platform to browse and purchase products.
- **Vendor**: The entity responsible for adding and managing product listings and processing orders.
- **Admin**: The person responsible for overseeing the platform's overall operations and user accounts.
- **UI**: User Interface.
- **URD**: User Requirements Document.

### 1.4 References
- [Project.md](./Project.md)
- [Architecture.md](./Architecture.md)

---

## 2. User Stories and Requirements

### 2.1 Shoppers

#### 2.1.1 User Registration and Authentication
- **As a shopper**, I want to create an account using my email or phone number so that I can access personalized shopping features.
- **As a shopper**, I want to reset my password easily if I forget it so that I can regain access quickly.
- **As a shopper**, I want to log in using Google or Apple for a faster sign-in experience.

#### 2.1.2 Product Search and Browsing
- **As a shopper**, I want to search for specific products by name or category so that I can find items quickly.
- **As a shopper**, I want to filter and sort products by price, ratings, and brand so that I can make informed purchasing decisions.
- **As a shopper**, I want to see product recommendations based on my browsing and purchase history so that I can discover relevant products.

#### 2.1.3 Product Information and Reviews
- **As a shopper**, I want to view detailed product information including price, size options, and images so that I can evaluate if it suits my needs.
- **As a shopper**, I want to read reviews and ratings from other shoppers so that I can trust the product quality.

#### 2.1.4 Shopping Cart
- **As a shopper**, I want to add products to my cart and modify quantities so that I can manage my selections before checking out.
- **As a shopper**, I want to save items in my cart for later so that I can purchase them when I’m ready.

#### 2.1.5 Checkout and Payment
- **As a shopper**, I want to check out using multiple payment methods (credit/debit card, e-wallets, or cash on delivery) so that I can select the most convenient option.
- **As a shopper**, I want to review my order before making payment so that I can confirm everything is correct.
- **As a shopper**, I want to receive an order confirmation immediately after placing my order so that I know it was successful.

#### 2.1.6 Order Tracking
- **As a shopper**, I want to track my order in real-time so that I know when my delivery will arrive.
- **As a shopper**, I want to receive updates when my order is shipped, out for delivery, and delivered.

#### 2.1.7 Order History and Payment History
- **As a shopper**, I want to view my previous orders and payment history, including product details, delivery dates, and payment methods used, so that I can track my purchases.

#### 2.1.8 Customer Support
- **As a shopper**, I want to contact customer support via email, phone, or live chat so that I can resolve any issues with my order.
- **As a shopper**, I want access to a help center with FAQs so that I can quickly find solutions to common issues.

---

### 2.2 Vendor

#### 2.2.1 Vendor Registration and Authentication
- **As a vendor**, I want to register for the platform so that I can list my products and manage my store.
- **As a vendor**, I want to log in securely using my registered email and password so that I can access the admin panel.

#### 2.2.2 Product Management
- **As a vendor**, I want to add, edit, or remove products from my store so that I can keep my catalog up to date.
- **As a vendor**, I want to manage product details including price, quantity, description, and images so that my products are accurately represented to shoppers.

#### 2.2.3 Order Management
- **As a vendor**, I want to view all the orders placed for my products so that I can track sales and shipments.
- **As a vendor**, I want to update the order status (e.g., shipped, delivered) so that shoppers are informed about their order progress.
- **As a vendor**, I want to process returns and refunds for any orders that require them.

#### 2.2.4 Payment Management
- **As a vendor**, I want to receive timely payments for the orders placed by shoppers so that I can manage my finances efficiently.
- **As a vendor**, I want to view a payment history of all completed transactions so that I can manage my revenue and reconcile finances.

#### 2.2.5 Customer Support
- **As a vendor**, I want to contact Mynthra support for issues related to my products, store management, or order fulfillment.

---

### 2.3 Admin

#### 2.3.1 User and Vendor Management
- **As an admin**, I want to manage vendor registrations and approve or reject vendor accounts so that only valid vendors can sell products.
- **As an admin**, I want to manage shopper accounts, including viewing and deactivating accounts if necessary.

#### 2.3.2 Product Oversight
- **As an admin**, I want to oversee the products listed by vendors to ensure that they meet platform guidelines.

#### 2.3.3 Order Oversight
- **As an admin**, I want to view all orders across the platform to monitor sales and potential issues.

#### 2.3.4 Reporting and Analytics
- **As an admin**, I want to generate reports on product performance, order volumes, and revenue to analyze platform success.
- **As an admin**, I want to view insights into user behavior and platform trends to make informed business decisions.

#### 2.3.5 Platform Maintenance
- **As an admin**, I want to manage platform settings, such as payment gateway integrations, shipping options, and user permissions to ensure smooth operation.
- **As an admin**, I want to handle any technical issues that arise on the platform to ensure continuous operation.

---

## 3. User Interface Requirements

### 3.1 Product Search and Discovery
- A prominent search bar with real-time product suggestions.
- Filters for sorting by price, rating, brand, and availability.
- Personalized product recommendations based on browsing and purchasing history.

### 3.2 Product Page
- Clear product images, descriptions, pricing, and size options.
- Option for shoppers to submit product ratings and reviews.
- Real-time stock and size availability information.

### 3.3 Shopping Cart and Checkout
- Intuitive cart interface displaying product details, quantities, and total price.
- Multiple secure payment options.
- Review and confirmation screen before completing the order, displaying a breakdown of the selected products and final amount.

### 3.4 Order Tracking
- A visual status bar or map showing the real-time status of the order.
- Notifications for key stages of order processing (shipped, out for delivery, delivered).

### 3.5 Customer Support
- A help center with easy navigation for common FAQs.
- Contact options for live chat, email, and phone support.

---

## 4. Conclusion
Mynthra 2.0 aims to provide a seamless and efficient shopping experience for shoppers, vendors, and administrators alike. This document outlines the requirements and user stories to ensure that each user role has the tools and features needed to interact with the platform effectively. With a focus on usability, convenience, and support, Mynthra 2.0 will empower all stakeholders to manage and participate in the shopping ecosystem with ease.
