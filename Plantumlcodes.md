# System Context  Diagram Code

```plantuml
@startuml
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Context.puml

LAYOUT_WITH_LEGEND()
title System Context Diagram - Mynthra 2.0

Person(shopper, "Shopper", "Browses products, places orders, tracks deliveries")
Person(vendor, "Vendor", "Manages product catalog, processes orders")
Person(admin, "Admin", "Manages platform, oversees activities")
System(mynthraPlatform, "Mynthra 2.0 Platform", "E-commerce platform for browsing, purchasing, and delivery management")

System_Ext(paymentGateway, "Payment Gateway", "Handles secure payment transactions")
System_Ext(logisticsAPI, "Logistics API", "Handles shipment and delivery tracking, including shipper management")
System_Ext(smsEmailAPI, "SMS/Email Service", "Sends notifications to users")
System_Ext(inventorySystem, "Inventory Management System", "Manages product stock levels")
System_Ext(analyticsService, "Analytics Service", "Tracks user activity and performance")

Rel(shopper, mynthraPlatform, "Uses", "HTTPS")
Rel(vendor, mynthraPlatform, "Manages catalog and orders", "HTTPS")
Rel(admin, mynthraPlatform, "Manages platform", "HTTPS")

Rel(mynthraPlatform, paymentGateway, "Processes payments", "API")
Rel(mynthraPlatform, logisticsAPI, "Tracks delivery", "API")
Rel(mynthraPlatform, smsEmailAPI, "Sends notifications", "API")
Rel(mynthraPlatform, inventorySystem, "Manages product stock", "API")
Rel(mynthraPlatform, analyticsService, "Tracks usage", "API")
@enduml
```
# Container Diagram Code


```plantuml
@startuml
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Container.puml

LAYOUT_WITH_LEGEND()
title Container Diagram - Mynthra 2.0

Person(shopper, "Shopper", "Browses and purchases products")
Person(vendor, "Vendor", "Manages product listings and orders")
Person(admin, "Admin", "Manages the platform")

System_Boundary(mynthra, "Mynthra 2.0") {
    Container(web, "Web Application", "React", "Browser-based interface")
    Container(mobile, "Mobile App", "React Native", "Mobile interface")
    Container(api, "API Gateway", "Node.js", "API routing layer")
    
    Container(product, "Product Service", "Node.js", "Product catalog and management")
    Container(user, "User Service", "Node.js", "User management")
    Container(cart, "Cart Service", "Node.js", "Shopping cart management")
    Container(order, "Order Service", "Node.js", "Order management")
    Container(payment, "Payment Service", "Node.js", "Payment processing")
    Container(notification, "Notification Service", "Node.js", "Push notifications")
    Container(rating, "Rating and Review Service", "Node.js", "Product and vendor reviews")
    Container(shipping, "Shipping Service", "Node.js", "Order delivery and tracking")
    
    ContainerDb(productdb, "Product DB", "MongoDB", "Product data")
    ContainerDb(userdb, "User DB", "PostgreSQL", "User data")
    ContainerDb(orderdb, "Order DB", "PostgreSQL", "Order data")
    ContainerDb(cartdb, "Cart DB", "MongoDB", "Cart data")
    ContainerDb(cache, "Cache", "Redis", "Data caching")
    ContainerDb(queue, "Message Queue", "RabbitMQ", "Event processing")
}

System_Ext(payment_gateway, "Payment Gateway", "Payment processing")
System_Ext(logistics_api, "Logistics API", "Shipping services and order tracking")
System_Ext(sms_email, "SMS/Email Notifications", "Order confirmations and updates")

Rel(shopper, web, "Uses", "HTTPS")
Rel(shopper, mobile, "Uses", "HTTPS")
Rel(vendor, web, "Uses", "HTTPS")
Rel(vendor, mobile, "Uses", "HTTPS")
Rel(admin, web, "Uses", "HTTPS")

Rel(web, api, "Uses", "HTTPS")
Rel(mobile, api, "Uses", "HTTPS")

Rel(api, product, "Uses", "gRPC")
Rel(api, user, "Uses", "gRPC")
Rel(api, cart, "Uses", "gRPC")
Rel(api, order, "Uses", "gRPC")
Rel(api, payment, "Uses", "gRPC")
Rel(api, rating, "Uses", "gRPC")
Rel(api, shipping, "Uses", "gRPC")

Rel(product, productdb, "Reads/Writes", "MongoDB Wire")
Rel(user, userdb, "Reads/Writes", "PostgreSQL")
Rel(cart, cartdb, "Reads/Writes", "MongoDB Wire")
Rel(order, orderdb, "Reads/Writes", "PostgreSQL")
Rel(notification, queue, "Subscribes", "AMQP")
Rel(rating, productdb, "Reads/Writes", "MongoDB Wire")

Rel(payment, payment_gateway, "Processes", "API")
Rel(shipping, logistics_api, "Tracks and updates delivery status", "API")
Rel(notification, sms_email, "Sends notifications", "API")

Rel(product, queue, "Publishes", "AMQP")
Rel(order, queue, "Publishes", "AMQP")
@enduml
```
#component diagram

```
@startuml
skinparam componentStyle rectangle

title Component Diagram for Myntra 2.0

' Users and roles
actor Shopper
actor Vendor
actor Admin

' Components
package "Frontend" {
    [Shopper UI] <<Component>> 
    [Vendor Dashboard] <<Component>> 
    [Admin Panel] <<Component>> 
}

package "Backend" {
    [Authentication Service] <<Component>>
    [Product Catalog Service] <<Component>>
    [Shopping Cart Service] <<Component>>
    [Order Management Service] <<Component>>
    [Payment Processing Service] <<Component>>
    [Order Tracking Service] <<Component>>
    [Notification Service] <<Component>>
    [Ratings and Reviews Service] <<Component>>
}

package "External Systems" {
    [Payment Gateway] <<External>>
    [Logistics API] <<External>>
    [Email/SMS API] <<External>>
}

' Relationships
Shopper --> [Shopper UI]
Vendor --> [Vendor Dashboard]
Admin --> [Admin Panel]

[Shopper UI] --> [Authentication Service]
[Shopper UI] --> [Product Catalog Service]
[Shopper UI] --> [Shopping Cart Service]
[Shopper UI] --> [Order Management Service]
[Shopper UI] --> [Order Tracking Service]
[Shopper UI] --> [Ratings and Reviews Service]

[Vendor Dashboard] --> [Authentication Service]
[Vendor Dashboard] --> [Product Catalog Service]
[Vendor Dashboard] --> [Order Management Service]
[Vendor Dashboard] --> [Ratings and Reviews Service]

[Admin Panel] --> [Authentication Service]
[Admin Panel] --> [Product Catalog Service]
[Admin Panel] --> [Order Management Service]
[Admin Panel] --> [Notification Service]

[Order Management Service] --> [Payment Processing Service]
[Order Management Service] --> [Notification Service]
[Order Management Service] --> [Order Tracking Service]

[Payment Processing Service] --> [Payment Gateway]

[Order Tracking Service] --> [Logistics API]

[Notification Service] --> [Email/SMS API]

@enduml

```
#deployement diagram 
```
 @startuml
!define RECTANGLE class
!define NODE node
!define COMPONENT component

' Define nodes and components for deployment
NODE WebServer {
    COMPONENT WebApplication {
        [Frontend: React/Next.js]
    }
    COMPONENT API {
        [Backend: Node.js/Express]
    }
}

NODE DatabaseServer {
    COMPONENT Database {
        [MongoDB/PostgreSQL]
    }
}

NODE PaymentService {
    COMPONENT PaymentGateway {
        [Razorpay/Stripe API]
    }
}

NODE NotificationService {
    COMPONENT NotificationSystem {
        [SMS/Email API]
    }
}

NODE LogisticsService {
    COMPONENT LogisticsAPI {
        [Logistics API]
    }
}

NODE MobileApp {
    COMPONENT MobileClient {
        [Android/iOS App]
    }
}

' Define relationships between nodes and components
WebApplication --> API : Calls API for data
API --> Database : Interacts with Database
API --> PaymentGateway : Processes payments
API --> NotificationSystem : Sends notifications
API --> LogisticsAPI : Retrieves logistics info

MobileClient --> WebApplication : Accesses Web Application for UI
MobileClient --> API : Interacts for data and actions

' Show external connections
DatabaseServer -[hidden]-> WebServer : Data flow
PaymentService -[hidden]-> WebServer : Payment processing
NotificationService -[hidden]-> WebServer : Notification handling
LogisticsService -[hidden]-> WebServer : Shipment tracking

@enduml
```
