@startuml
left to right direction
actor Shopper
actor Vendor
actor Admin

usecase "Register Account" as UC1
usecase "Login to Platform" as UC2
usecase "View Product Catalog" as UC3
usecase "Add Product to Cart" as UC4
usecase "Place Order" as UC5
usecase "Make Payment" as UC6
usecase "Track Order" as UC7
usecase "Rate and Review Products" as UC8
usecase "Manage Product Listings" as UC9
usecase "Process Orders" as UC10
usecase "Manage User Accounts" as UC11

Shopper --> UC1
Shopper --> UC2
Shopper --> UC3
Shopper --> UC4
Shopper --> UC5
Shopper --> UC6
Shopper --> UC7
Shopper --> UC8

Vendor --> UC2
Vendor --> UC3
Vendor --> UC9
Vendor --> UC10

Admin --> UC2
Admin --> UC11

UC1 --> UC2 : <<includes>>
UC5 --> UC6 : <<includes>>
UC7 --> UC2 : <<includes>>

@enduml
