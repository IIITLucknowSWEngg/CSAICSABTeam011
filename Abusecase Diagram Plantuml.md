@startuml
title Abuse Case Diagram for Myntra 2.0


left to right direction

actor Hacker
actor Customer
actor "Delivery Person" as DeliveryPerson

rectangle "Myntra App System" {
    usecase "Place Order" as UC1
    usecase "Make Payment" as UC2
    usecase "Track Order" as UC3
    usecase "Cancel Order Fraudulently" as UC4
    usecase "Steal Payment Information" as UC5
    usecase "Fake Account Creation" as UC6
}

Hacker --> UC4
Hacker --> UC5
Hacker --> UC6

UC4 -down-> UC1 : <<threatens>>
UC5 -down-> UC2 : <<threatens>>
UC6 -down-> UC3 : <<threatens>>

Customer --> UC1
Customer --> UC2
Customer --> UC3

DeliveryPerson --> UC3 : Assist

@enduml

