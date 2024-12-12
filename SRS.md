# Software Requirements Specification (SRS) Document

## 1. Introduction

### 1.1 Purpose
This Software Requirements Specification (SRS) document outlines the functional and non-functional requirements for the Mynthra e-commerce platform. It serves as a guide for developers, testers, and stakeholders throughout the software development lifecycle, ensuring the platform meets the needs of shoppers, vendor, and administrators.

### 1.2 Scope
The Mynthra e-commerce platform enables users to browse, purchase, and manage products such as clothing, footwear, and accessories. The system will handle user registration, product browsing, order placement, payment processing, and order tracking. This SRS covers the functional and non-functional requirements, user interfaces, external interfaces, and design constraints for the development and implementation of Mynthra.

### 1.3 Definitions, Acronyms, and Abbreviations
- SRS: Software Requirements Specification  
- UI: User Interface  
- SKU: Stock Keeping Unit  
- API: Application Programming Interface  
- OTP: One-Time Password  
- NFR: Non-Functional Requirement  
- Shopper: A person using the platform to browse products, make purchases, and track deliveries  
- Vendor: A business or individual offering products on the platform

### 1.4 References
- IEEE Std 830-1998, IEEE Recommended Practice for Software Requirements Specifications  
- SWEBOK v3.0, Software Engineering Body of Knowledge  
- Stakeholders.md  
- User Requirements Document

### 1.5 Overview
This document is structured into several sections that define the system's overall description, functional and non-functional requirements, external interfaces, and design constraints relevant to the development of the Mynthra platform.

---

## 2. Overall Description

### 2.1 Product Perspective
The Mynthra platform is an e-commerce system designed to operate on both mobile and desktop devices. It interfaces with external systems such as payment gateways, inventory management systems, and third-party APIs for logistics and shipping. The platform will be modular in design, allowing for easy scaling and feature expansion.

### 2.2 Product Functions
- User registration and authentication.  
- Product catalog management (by vendor).  
- Shopping cart and order management.  
- Real-time order tracking and delivery management.  
- Payment processing and history tracking.  
- Ratings and Reviews.

### 2.3 User Classes and Characteristics
- Shoppers: Individuals using the platform to browse products, place orders, and track deliveries.  
- Vendor: Businesses managing product listings, orders, and stock availability.  
- Admins: Individuals managing the platform, overseeing user, vendor, and order activities.

### 2.4 Operating Environment
The Mynthra platform will operate on web browsers and mobile applications (Android and iOS). It requires internet connectivity for functionalities such as product browsing, checkout, and order tracking. The backend will be hosted on cloud services for high availability and scalability.

- Web Browsers: The platform supports the latest versions of popular web browsers, including Chrome, Firefox, Safari, and Microsoft Edge.
- Mobile Applications:
  - Android: The mobile app will support Android 8.0 (Oreo) and higher versions.
  - iOS: The mobile app will support iOS 12.0 and later versions.

### 2.5 Design and Implementation Constraints
- The platform must comply with data protection laws (e.g., GDPR).
- Performance constraints are dictated by mobile devices' capabilities.
- External services such as payment gateways and logistics providers will need to be integrated smoothly.
- The platform will initially only support one currency (INR) and one language (English).

### 2.6 Assumptions and Dependencies
- Shoppers and vendor have access to devices with stable internet connections.
- Third-party service integrations for payment, logistics, and notifications will be reliable.  
- The system will initially support domestic transactions only.  
- The platform assumes that third-party services (e.g., payment gateways, shipping APIs) will be available and reliable for integration. Any downtime or outages from these services will need to be handled by fallback mechanisms or error notifications.

---

## 3. System Features

### 3.1 User Registration and Authentication
Description: Shoppers, Vendor, and Admins will be able to create accounts, log in, and manage their profiles securely.

Functional Requirements:
- The system shall allow users to register with email, phone number, or social logins (e.g., Google, Facebook).
- The system shall send an OTP for account verification.
- The system shall support secure password recovery via email or SMS.
- Shoppers shall be able to manage their profiles, including personal information, saved addresses, order history, and payment preferences.
- Vendor shall be able to manage their profiles, including business information and product catalog.

### 3.2 Product Catalog Browsing
Description: Shoppers can search, filter, and browse products by categories, brands, prices, and ratings.

Functional Requirements:
- The system shall allow shoppers to browse products by category (e.g., clothing, accessories, footwear).
- The system shall provide search and filter functionalities (e.g., price range, brand, size).
- The system shall display product details, including price, SKU, description, and customer reviews.
- Vendor shall be able to add, update, and remove products from their catalog and manage product availability.

### 3.3 Shopping Cart Management
Description: Shoppers can add, remove, and review products in their shopping cart before proceeding to checkout.

Functional Requirements:
- The system shall allow shoppers to add and remove items from the shopping cart.
- The system shall display the total cost of items, including taxes and shipping fees.
- The system shall allow users to modify the quantity of items in the cart.

### 3.4 Order Placement and Checkout
Description: Shoppers can complete their purchase by submitting orders and making payments.

Functional Requirements:
- The system shall provide multiple payment methods (credit card, UPI, net banking).
- The system shall confirm the order after successful payment.
- The system shall send an order confirmation email/SMS to the shopper.
- Vendor shall be notified when an order is placed for their products and shall have the ability to process the order.

### 3.5 Payment Processing
Description: The system processes payments securely and maintains payment history for shoppers.

Functional Requirements:
- The system shall integrate with secure payment gateways.
- The system shall store a payment history for shoppers to review past transactions.
- The system shall automatically deduct the amount upon order confirmation.
- Vendor shall receive their payment after the order is successfully placed and processed.

### 3.6 Order Tracking
Description: Shoppers can track the status of their orders in real-time.

Functional Requirements:
- The system shall provide real-time order tracking, including shipment status and estimated delivery time.
- The system shall send notifications when the order status changes (e.g., shipped, out for delivery).

### 3.7 Ratings and Reviews
Description: Shoppers can provide feedback on products and sellers after completing purchases.

Functional Requirements:
- The system shall allow users to rate and review products and sellers after an order is delivered.
- The system shall display average product ratings and reviews on product pages.
- Vendor shall be able to view ratings and reviews left by shoppers for their products and services.

---

## 4. External Interface Requirements

### 4.1 User Interfaces
- Shopper UI: The platform will offer a user-friendly, responsive interface for product browsing, shopping cart management, and checkout. It will be designed to work across both mobile and desktop devices.
  - Mobile Devices: The mobile app interface will support Android 8.0 and above, and iOS 12.0 and above.
  - Web Browsers: The platform will be fully compatible with the latest versions of web browsers (e.g., Chrome, Firefox, Safari, and Edge).
  
- Vendor Dashboard: A web-based interface for sellers to manage product listings, track orders, and review sales performance.

- Admin Panel: A comprehensive web dashboard for administrators to manage shoppers, orders, and system settings.

### 4.2 Hardware Interfaces
The system will interact with the following hardware:
- Mobile Devices: For accessing the mobile app.
- GPS Modules: To track delivery statuses in real-time.
- Cameras: Used for profile pictures or uploading product images.

### 4.3 Software Interfaces
The system will integrate with the following external services:
- Payment Gateways: For secure transaction processing.
- Logistics APIs: To manage order shipping, tracking, and delivery status updates.
- SMS/Email APIs: For sending notifications to users (e.g., order updates, delivery status).

### 4.4 Communication Interfaces
- The platform will use secure HTTPS protocols to protect user data.
- It will use WebSocket for real-time notifications (e.g., order status updates, shipment tracking updates).

# 5. Use Cases

## 5.1 Use Case: Shoppers Registration
*Primary Actor:* New Shopper  
*Preconditions:* Shopper has a valid email address  

*Main Flow:*
1. Shopper navigates to the registration page.
2. Shopper enters personal details (name, email, password).
3. System validates input.
4. System creates a shopper account.
5. System sends a verification email.
6. Shopper verifies the email.
7. Shopper can now log in.

*Alternative Flow:*
- If input is invalid (e.g., email format is incorrect), the system prompts the shopper to correct the input.
- If email verification fails, the system prompts the shopper to resend the verification email.

## 5.2 Use Case: Shoppers Login
*Primary Actor:* Registered Shopper  
*Preconditions:* Shopper has a verified account  

*Main Flow:*
1. Shopper enters email and password.
2. System validates credentials.
3. System generates authentication token and logs the shopper in.
4. Shopper is redirected to the homepage or dashboard.

*Alternative Flow:*
- If credentials are incorrect, the system prompts the shopper to re-enter the details or reset the password.

## 5.3 Use Case: Product Catalog Browsing
*Primary Actor:* Shopper  
*Preconditions:* Shopper is logged in  

*Main Flow:*
1. Shopper navigates to the product catalog.
2. Shopper filters products by categories, brand, size, or price range.
3. System displays the filtered list of products with details (price, description, SKU).
4. Shopper selects a product to view details.

*Alternative Flow:*
- If no products match the filters, the system displays a message indicating no results found.

## 5.4 Use Case: Shopping Cart Management
*Primary Actor:* Shopper  
*Preconditions:* Shopper has at least one product in their cart  

*Main Flow:*
1. Shopper adds items to the shopping cart.
2. System updates the cart with the added item.
3. Shopper views the cart and can modify the quantity or remove items.
4. Shopper proceeds to checkout.

*Alternative Flow:*
- If the shopper tries to remove an item that is not in the cart, the system displays a message stating the item is not in the cart.

## 5.5 Use Case: Order Placement
*Primary Actor:* Shopper  
*Preconditions:* Shopper has items in the cart  

*Main Flow:*
1. Shopper proceeds to checkout.
2. Shopper reviews the order summary (items, price, shipping).
3. Shopper enters shipping details.
4. Shopper selects a payment method and enters payment details.
5. System processes the payment.
6. System confirms the order and sends an email confirmation to the shopper.

*Alternative Flow:*
- If payment fails, the system prompts the shopper to retry or use a different payment method.

## 5.6 Use Case: Payment Processing
*Primary Actor:* Shopper  
*Preconditions:* Shopper has placed an order and provided payment details  

*Main Flow:*
1. Shopper selects a payment method (credit card, PayPal, etc.).
2. Shopper enters payment details (card number, CVV, etc.).
3. System validates payment details.
4. System processes the payment with the selected payment gateway.
5. System confirms payment success and proceeds to order confirmation.

*Alternative Flow:*
- If the payment fails, the system prompts the shopper to retry or use a different payment method.

## 5.7 Use Case: Order Tracking
*Primary Actor:* Shopper  
*Preconditions:* Shopper has placed an order  

*Main Flow:*
1. Shopper navigates to the order tracking page.
2. Shopper selects an order to view the status.
3. System displays the order’s current status (e.g., processing, shipped, delivered).
4. System provides an estimated delivery time and tracking information (if available).

*Alternative Flow:*
- If the order has not shipped yet, the system shows an estimated processing time.

## 5.8 Use Case: Vendor Login
*Primary Actor:* Registered Vendor  
*Preconditions:* Vendor has a verified account  

*Main Flow:*
1. Vendor enters email and password.
2. System validates credentials.
3. System generates authentication token and logs the vendor in.
4. Vendor is redirected to the vendor dashboard.

*Alternative Flow:*
- If credentials are incorrect, the system prompts the vendor to re-enter the details or reset the password.

## 5.9 Use Case: Vendor Product Catalog Management
*Primary Actor:* Vendor  
*Preconditions:* Vendor is logged in  

*Main Flow:*
1. Vendor navigates to the product catalog management page.
2. Vendor adds, updates, or removes products.
3. Vendor manages product details (name, price, description, quantity).
4. Vendor saves the changes, and the product catalog is updated.

*Alternative Flow:*
- If required fields are missing (e.g., product name or price), the system prompts the vendor to complete the form.

## 5.10 Use Case: Vendor Order Management
*Primary Actor:* Vendor  
*Preconditions:* Vendor is logged in  

*Main Flow:*
1. Vendor navigates to the order management page.
2. Vendor reviews orders placed by shoppers.
3. Vendor can update the order status (e.g., processing, shipped).
4. Vendor can cancel orders or issue refunds.

*Alternative Flow:*
- If the vendor attempts to update an order status that is already completed (e.g., delivered), the system prevents the update and shows an error message.

## 5.11 Use Case: Admin Registration in App
*Primary Actor:* Admin  
*Preconditions:* Admin has valid registration details  

*Main Flow:*
1. Admin navigates to the registration page.
2. Admin enters personal details (name, email, password).
3. System validates input.
4. System creates an admin account.
5. System sends a verification email.
6. Admin verifies the email and completes registration.

*Alternative Flow:*
- If the input is invalid (e.g., email format is incorrect), the system prompts the admin to correct the input.
- If email verification fails, the system prompts the admin to resend the verification email.

## 5.12 Use Case: Admin Login
*Primary Actor:* Admin  
*Preconditions:* Admin has a verified account  

*Main Flow:*
1. Admin enters email and password.
2. System validates credentials.
3. System generates authentication token and logs the admin in.
4. Admin is redirected to the admin dashboard.

*Alternative Flow:*
- If credentials are incorrect, the system prompts the admin to re-enter the details or reset the password.

## 5.13 Use Case: Admin Order Management
*Primary Actor:* Admin  
*Preconditions:* Admin is logged in  

*Main Flow:*
1. Admin navigates to the order management page.
2. Admin reviews orders placed by shoppers.
3. Admin can update the order status (e.g., processing, shipped).
4. Admin can cancel orders or issue refunds.

*Alternative Flow:*
- If the admin attempts to update an order status that is already completed (e.g., delivered), the system prevents the update and shows an error message.

---

## 6. Non-Functional Requirements

### 6.1 Performance
- The platform should load pages within 3 seconds under typical network conditions (e.g., 3G or Wi-Fi).
- The system must handle up to 1000 concurrent users without performance degradation.

### 6.2 Security
- Data shall be encrypted in transit (TLS) and at rest (AES-256).
- The system shall enforce strong password policies and support multi-factor authentication.

### 6.3 Usability
- The app and website shall follow WCAG 2.1 accessibility guidelines.

### 6.4 Scalability
- The system must support future growth in terms of both user base and product listings without significant performance issues.

### 6.5 Reliability
- The platform must ensure an uptime of 99.9%, with minimal downtime for maintenance.

---

## 7. Assumptions and Dependencies
- The platform assumes that shoppers will have access to modern web browsers and smartphones with internet connectivity.
- The system relies on third-party services for payment processing and shipping integration. Any downtime or outages from these services will be managed through fallback mechanisms or error notifications.

---

## 8. Conclusion
This document defines the functional and non-functional requirements for the Mynthra e-commerce platform. It ensures that the development team can build the platform according to user expectations and business objectives.
