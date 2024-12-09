# User Requirements Document (URD)

## Overview

This document outlines the user requirements for a Myntra clone, an e-commerce platform designed to provide a seamless shopping experience for fashion lovers. The platform will cater to three main user personas: shoppers, a single seller, and admins, ensuring intuitive browsing, filtering, and order placement features. The focus is on delivering an efficient, user-friendly interface for exploring, selecting, and purchasing fashion products while allowing users to manage their accounts, wishlists, and order tracking. The platform will support only **one seller** who will provide all the products listed for sale. 

---

## Table of Contents

1. [User Personas](#user-personas)  
2. [User Stories](#user-stories)  
3. [Use Cases](#use-cases)  
4. [Assumptions and Dependencies](#assumptions-and-dependencies)  
5. [Glossary](#glossary)  

---

## 5. User Personas

### Persona 1: Fashion Enthusiast (Shopper)
- **Name**: Meera  
- **Age**: 25  
- **Occupation**: Marketing Executive  
- **Tech Skills**: Moderate  
- **Needs**: Wants a simple, visually appealing platform to explore the latest fashion trends and make quick purchases. Meera prefers mobile shopping and relies on a smooth and easy-to-navigate user experience.

### Persona 2: Budget-Conscious Shopper
- **Name**: Rahul  
- **Age**: 30  
- **Occupation**: Engineer  
- **Tech Skills**: High  
- **Needs**: Looks for discounts and budget-friendly products. Rahul frequently filters products by price and uses coupons during checkout.

### Persona 3: Seller (Single Vendor)
- **Name**: Priya  
- **Age**: 35  
- **Occupation**: Boutique Owner  
- **Tech Skills**: Low  
- **Needs**: As the sole seller on the platform, Priya needs a straightforward way to upload new products, manage inventory, track orders, and monitor product performance. Priya relies on a simple dashboard to view sales and customer feedback.

### Persona 4: Admin
- **Name**: Arjun  
- **Age**: 40  
- **Occupation**: E-commerce Manager  
- **Tech Skills**: High  
- **Needs**: Requires a comprehensive platform to monitor overall performance, manage shopper interactions, resolve complaints, and oversee website functionality. Arjun also ensures the platform runs smoothly by handling operational tasks.
  
### Persona 5: Shipper
- **Name**: Ravi  
- **Age**: 32  
- **Occupation**: Logistics Manager  
- **Tech Skills**: Moderate  
- **Needs**: Ravi needs an efficient system to manage and track shipments. He requires notifications for new orders and updates on delivery status, along with tools to handle customer complaints related to shipping and delays.

---

## 6. User Stories

- **User Story 1**: As a shopper, I want to browse through a variety of clothing categories so that I can find items that suit my taste and needs.
- **User Story 2**: As a shopper, I want to filter products based on size, color, and price so that I can quickly find what I am looking for.
- **User Story 3**: As a shopper, I want to add multiple items to my shopping cart so that I can purchase them in one go.
- **User Story 4**: As a shopper, I want to save my favorite products to a wishlist so that I can purchase them later.
- **User Story 5**: As a seller, I want to upload new products to the platform so that I can showcase my inventory to shoppers.
- **User Story 6**: As a seller, I want to track my product sales and inventory so that I can manage my stock effectively.
- **User Story 7**: As an admin, I want to monitor and manage shopper activity on the platform so that I can ensure smooth operations and a positive experience for shoppers.
- **User Story 8**: As an admin, I want to resolve shopper complaints and issues with orders so that the platform maintains a good reputation.
- **User Story 9**: As a shipper, I want to receive notifications for new orders and updates on delivery status so that I can manage shipments effectively.
- **User Story 10**: As a shipper, I want to handle customer complaints related to shipping and delays so that the delivery process is smooth and efficient.

---

## 7. Use Cases

### **Use Case 1: Shopper Registration**
- **Actors**: Shopper  
- **Goal**: Enable a shopper to create an account on the platform.  
- **Precondition**: The shopper must have a valid email address or phone number.  
- **Basic Flow**:  
  1. Shopper navigates to the registration page.  
  2. Shopper fills in their name, email/phone number, and password.  
  3. Shopper submits the registration form.  
  4. The system sends a verification email/SMS.  
  5. Shopper verifies their email/phone, and the account is created.  
- **Postcondition**: Shopper can log in and access the platform's features.  
- **Exceptions**: If the shopper’s email/phone is already registered, an error message is displayed.

### **Use Case 2: Seller Product Upload**
- **Actors**: Seller  
- **Goal**: Allow the seller to upload new products to the platform.  
- **Precondition**: The seller must have a registered account and be logged in.  
- **Basic Flow**:  
  1. Seller navigates to the product upload page.  
  2. Seller fills in the product details (name, category, price, stock, images).  
  3. Seller submits the product listing.  
  4. The system verifies the details and lists the product in the appropriate category.  
- **Postcondition**: The product is available for shoppers to browse and purchase.  
- **Exceptions**: If required details are missing, the system prompts the seller to complete the information.

### **Use Case 3: Admin Resolves Complaint**
- **Actors**: Admin  
- **Goal**: Enable the admin to resolve shopper complaints regarding orders or platform usage.  
- **Precondition**: Admin must be logged in with appropriate privileges.  
- **Basic Flow**:  
  1. Admin navigates to the complaints section.  
  2. Admin reviews the complaint details (shopper ID, order ID, issue).  
  3. Admin contacts the seller or takes necessary action to resolve the issue.  
  4. Admin updates the complaint status.  
- **Postcondition**: Shopper receives a resolution, and the complaint is marked as resolved.  
- **Exceptions**: If the complaint cannot be resolved, the admin may escalate the issue for further investigation.

### **Use Case 4: Shipper Tracks Shipments**
- **Actors**: Shipper  
- **Goal**: Enable the shipper to track the status of orders and handle shipping-related issues.  
- **Precondition**: Shipper must be logged in and assigned to manage specific shipments.  
- **Basic Flow**:  
  1. Shipper receives notification of a new order.  
  2. Shipper tracks the shipment progress and updates the status as necessary.  
  3. Shipper notifies the customer about shipping delays or issues.  
  4. Shipper handles customer complaints related to shipping.  
- **Postcondition**: Shipment is delivered, and any shipping issues are resolved.  
- **Exceptions**: If there are delays, the system prompts the shipper to notify the shopper.

---
---

## 8. Assumptions and Dependencies

- Shoppers, the seller, shippers and admins will have internet access and devices that support a modern web browser.
- The platform will integrate with third-party payment gateways for order processing.
- Product availability and inventory will be managed by the single seller and updated accordingly.

---

## 9. Glossary

- **Shopper**: A user who visits the platform to browse or purchase products.
- **Seller**: A single vendor or boutique that provides all the products listed for sale on the platform.
- **Admin**: A user responsible for managing the platform, including overseeing shopper activities, handling complaints, and ensuring smooth operations.
- **Shipper**: A logistics manager responsible for managing and tracking shipments, handling complaints, and ensuring timely delivery.
- **Cart**: A feature where shoppers can store products they intend to purchase.
- **Wishlist**: A feature allowing shoppers to save products for future purchases.
- **Checkout**: The process of completing a purchase, including payment and delivery details.
