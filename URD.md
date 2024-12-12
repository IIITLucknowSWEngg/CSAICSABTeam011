# User Requirements Document (URD)

## Overview

This document outlines the user requirements for Myntra 2.0, an e-commerce platform designed to provide a seamless shopping experience for fashion lovers. The platform will cater to three main user personas: shoppers, a single vendor, and admins, ensuring intuitive browsing, filtering, and order placement features. The focus is on delivering an efficient, user-friendly interface for exploring, selecting, and purchasing fashion products while allowing users to manage their accounts, wishlists, and order tracking. The platform will support only one vendor who will provide all the products listed for sale. 

---

## Table of Contents

1. [User Personas](#user-personas)  
2. [User Stories](#user-stories)  
3. [Use Cases](#use-cases)  
4. [Assumptions and Dependencies](#assumptions-and-dependencies)  
5. [Glossary](#glossary)  

---

## 1. User Personas

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

### Persona 3: Vendor
- **Name**: Priya  
- **Age**: 35  
- **Occupation**: Boutique Owner  
- **Tech Skills**: Low  
- **Needs**: Needs a straightforward way to upload new products, manage inventory, track orders, and monitor product performance. Priya relies on a simple dashboard to view sales and customer feedback.

### Persona 4: Admin
- **Name**: Arjun  
- **Age**: 40  
- **Occupation**: E-commerce Manager  
- **Tech Skills**: High  
- **Needs**: Requires a comprehensive platform to monitor overall performance, manage shopper interactions, resolve complaints, and oversee website functionality. Arjun also ensures the platform runs smoothly by handling operational tasks.
  
---

## 2. User Stories

- **User Story 1**: As a shopper, I want to browse through a variety of clothing categories so that I can find items that suit my taste and needs.
- **User Story 2**: As a shopper, I want to filter products based on size, color, and price so that I can quickly find what I am looking for.
- **User Story 3**: As a shopper, I want to add multiple items to my shopping cart so that I can purchase them in one go.
- **User Story 4**: As a shopper, I want to save my favorite products to a wishlist so that I can purchase them later.
- **User Story 5**: As a vendor, I want to upload new products to the platform so that I can showcase my inventory to shoppers.
- **User Story 6**: As a vendor, I want to track my product sales and inventory so that I can manage my stock effectively.
- **User Story 7**: As an admin, I want to monitor and manage shopper activity on the platform so that I can ensure smooth operations and a positive experience for shoppers.
- **User Story 8**: As an admin, I want to resolve shopper complaints and issues with orders so that the platform maintains a good reputation.

---

## 3. Use Cases
# Use Cases for Mynthra 2.0

## Use Case 1: Shopper Registers Account
- **Actors**: Shopper  
- **Goal**: Enable a new shopper to register on the platform.  
- **Precondition**: Shopper does not have an existing account.  
- **Basic Flow**:  
  1. Shopper clicks on "Sign Up" on the homepage.  
  2. Shopper provides personal information (name, email, password, etc.).  
  3. Shopper submits the registration form.  
  4. System creates a new account for the shopper and logs them in automatically.  
- **Postcondition**: Shopper has an account and is logged in.  
- **Exceptions**: If the email is already used, the shopper is asked to use a different email address.

## Use Case 2: Shopper Logs into Account
- **Actors**: Shopper  
- **Goal**: Allow a registered shopper to log into their account.  
- **Precondition**: Shopper has an existing account.  
- **Basic Flow**:  
  1. Shopper clicks on the "Login" button on the homepage.  
  2. Shopper enters their email and password.  
  3. Shopper clicks "Submit".  
  4. System validates the credentials and grants access.  
- **Postcondition**: Shopper is logged into their account.  
- **Exceptions**: If credentials are incorrect, an error message is displayed.

## Use Case 3: Shopper Browses Products
- **Actors**: Shopper  
- **Goal**: Allow the shopper to browse through available products on the platform.  
- **Precondition**: Shopper is logged in. 
- **Basic Flow**:  
  1. Shopper navigates to the homepage or a specific category.  
  2. Shopper views products displayed, with options to filter or sort by criteria (e.g., price, popularity).  
  3. Shopper selects a product to view detailed information.  
- **Postcondition**: Shopper can add the product to the cart or wishlist, or continue browsing.  
- **Exceptions**: If no products match the filters, a "No results found" message is displayed.

## Use Case 4: Shopper Adds Product to Cart
- **Actors**: Shopper  
- **Goal**: Allow the shopper to add products to their shopping cart for future purchase.  
- **Precondition**: Shopper has browsed and selected a product.  
- **Basic Flow**:  
  1. Shopper clicks on a product to view the product details.  
  2. Shopper selects size, quantity, and other options (if applicable).  
  3. Shopper clicks "Add to Cart."  
  4. The product is added to the shopper's cart.  
- **Postcondition**: The cart is updated with the new item, and the shopper can proceed to checkout or continue shopping.  
- **Exceptions**: If the product is out of stock or the quantity exceeds available stock, an error message is displayed.

## Use Case 5: Shopper Places an Order
- **Actors**: Shopper  
- **Goal**: Enable the shopper to place an order for the items in their cart.  
- **Precondition**: Shopper has items in their cart and is ready to check out.  
- **Basic Flow**:  
  1. Shopper navigates to the cart and reviews the selected products.  
  2. Shopper clicks "Proceed to Checkout" and selects a delivery address.  
  3. Shopper chooses a payment method and enters the required details.  
  4. Shopper confirms the order and completes the payment.  
- **Postcondition**: The system processes the order, generates a receipt, and the shopper receives an order confirmation.  
- **Exceptions**: If payment fails, an error message is displayed, and the shopper is prompted to retry or choose a different method.

## Use Case 7: Shopper Tracks an Order
- **Actors**: Shopper  
- **Goal**: Allow the shopper to track the status of their placed orders.  
- **Precondition**: Shopper has successfully placed an order.  
- **Basic Flow**:  
  1. Shopper logs into their account and navigates to the "Order History" section.  
  2. Shopper selects an order to view its status (e.g., confirmed, dispatched, delivered).  
  3. Shopper receives real-time updates as the order progresses.  
- **Postcondition**: The shopper can track their order from placement to delivery.  
- **Exceptions**: If tracking data is unavailable (e.g., due to delays), the system displays a message indicating the delay.

## Use Case 9: Admin Manages Products
- **Actors**: Admin  
- **Goal**: Allow the admin to add, edit, or remove products from the platform.  
- **Precondition**: Admin is logged in.  
- **Basic Flow**:  
  1. Admin logs into the admin panel.  
  2. Admin selects "Manage Products" from the menu.  
  3. Admin adds a new product or selects an existing product to edit or remove.  
  4. Admin saves the changes.  
- **Postcondition**: The product catalog is updated.  
- **Exceptions**: If an error occurs while saving changes, an error message is displayed.

## Use Case 10: Admin Manages Orders
- **Actors**: Admin  
- **Goal**: Enable the admin to view and manage shopper orders.  
- **Precondition**: Admin is logged in.  
- **Basic Flow**:  
  1. Admin logs into the admin panel.  
  2. Admin selects "Manage Orders" from the menu.  
  3. Admin reviews order details and updates the order status (e.g., dispatched, delivered).  
- **Postcondition**: The order status is updated.  
- **Exceptions**: If an error occurs while updating the order, an error message is displayed.

## Use Case 11: Admin Manages Users
- **Actors**: Admin  
- **Goal**: Allow the admin to manage shopper accounts.  
- **Precondition**: Admin is logged in.  
- **Basic Flow**:  
  1. Admin logs into the admin panel.  
  2. Admin selects "Manage Users" from the menu.  
  3. Admin views the list of registered shoppers, can deactivate or delete accounts.  
- **Postcondition**: The admin successfully manages shopper accounts.  
- **Exceptions**: If an error occurs while managing accounts, an error message is displayed.

## Use Case 12: Shopper Logs Out
- **Actors**: Shopper  
- **Goal**: Enable the shopper to log out of their account.  
- **Precondition**: Shopper is logged in.  
- **Basic Flow**:  
  1. Shopper clicks on the "Logout" button in their account menu.  
  2. Shopper is logged out and redirected to the homepage.  
- **Postcondition**: Shopper is logged out of the platform.  
- **Exceptions**: None.

---

## 4. Assumptions and Dependencies

- Shoppers, vendor, and admins will have internet access and devices that support a modern web browser.
- The platform will integrate with third-party payment gateways for order processing.
- Product availability and inventory will be managed by a single vendor and updated accordingly.

---

## 5. Glossary

- **Shopper**: A user who visits the platform to browse or purchase products.
- **Vendor**: A single vendor or boutique that provides all the products listed for sale on the platform.
- **Admin**: A user responsible for managing the platform, including overseeing shopper activities, handling complaints, and ensuring smooth operations.
- **Cart**: A feature where shoppers can store products they intend to purchase.
- **Wishlist**: A feature allowing shoppers to save products for future purchases.
- **Checkout**: The process of completing a purchase, including payment and delivery details.
