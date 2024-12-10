@startuml
left to right direction
skinparam packageStyle rectangle

actor Shopper as S
actor Vendor as V
actor Admin as A

package "Mynthra 2.0" {
    usecase "Browse Products" as UC1
    usecase "Search Products" as UC2
    usecase "View Product Details" as UC3
    usecase "Add to Cart" as UC4
    usecase "Checkout" as UC5
    usecase "Make Payment" as UC6
    usecase "Track Order" as UC7
    usecase "Provide Ratings & Reviews" as UC8
    usecase "Register or Login" as UC9
    usecase "Manage Account" as UC10

    usecase "Manage Product Listings" as UC11
    usecase "Manage Orders" as UC12
    usecase "Vendor Account Management" as UC16

    usecase "Manage Users" as UC13
    usecase "Manage Vendor" as UC14
    usecase "Manage Orders (Admin)" as UC15
    usecase "Notifications" as UC19
}

S --> UC9 : "Create or log in to account"
S --> UC1 : "Browse categories"
S --> UC2 : "Search for specific products"
UC1 --> UC3 : "Select a product"
UC2 --> UC3 : "View details of search results"
S --> UC4 : "Add selected products to cart"
S --> UC5 : "Review and confirm order"
UC5 --> UC6 : "Complete payment"
S --> UC7 : "Track order status"
S --> UC8 : "Rate and review product after delivery"
S --> UC10 : "Update profile, address, payment info"

V --> UC9 : "Register or log in as a vendor"
V --> UC11 : "Add, edit, or remove product listings"
V --> UC12 : "View and manage orders for products"
V --> UC16 : "Manage vendor account settings"

A --> UC13 : "Manage platform users"
A --> UC14 : "Oversee and manage vendors"
A --> UC15 : "Monitor and manage all orders"
A --> UC19 : "Send notifications to users"
@enduml
