## 1. **System Context Diagram**

![Myntra Clone - System Context Diagram](https://www.plantuml.com/plantuml/png/TPBDRjj038JlVWhM9nVmpwMddf8wGLkWBeJAFGUqH5iBx8_0fUpexSkLDh3Yk9T49fOVEJDyY88idREpJyPNjgi96f4sVjri62_hav6cEtIHk0fUoCkw2cxJMlIfPnMbjkQmsNvP5QdqT_Thup0AiPPUjgdZLTPjei_4Y2NOzLuOOMk39rX1sUjZ1_abF1ayCRhPh22EmI-gBafmn4kOR_FdNB-VVGrf9RWq0GuSBf4Ye1RRZgi6qw-MGzrL4jVppsymh9tnslsO_YVC3ZsUhc_1-BCA3Dml8N2jJSi16bfY51Fy09kDAo_S86JGeQYfh8H-1BL8Ze4Tw1y8tXfF49lGjiQV9foNvrTPg7HYZxR0tf6NxoXqmLunkG2vaiZxnd2zQf6bXpYw9o59g2YgbB4XRJeTK9CrP-A-q3O_sFcKAv1BEOd1tRmDHEApgMXGu99NkZfabA7R6Jw8EPfgSAeSEnNsUrA5NBwLCPqJoTTf33aqLWCeT-KoHniRcCp8QVmXExcIzw5y6ozZgL3Kkw2OIHRLgnmnT577AKb1-K9kAFbAxbz7liCQ1U5iy6sZTuJ_fpk6HjVOG1eEtQb93ltOxujIWHzu7yFSXi3gceBZ99-qq72BnSzxcFjvbUf_zWQgu8-6tUZsABPLfPHDkx8VjAbpzXy0)

```plantuml
@startuml
' External Actors
actor "Customer" as customer
actor "Admin" as admin

' System Boundary
package "Myntra Clone" {
  [Myntra Clone] as myntraClone
}

' External Systems
actor "Payment Gateway" as externalPaymentGateway
actor "Delivery Partner" as deliveryPartner
actor "Notification Service" as notificationService

' Relationships
customer --> myntraClone : Browses and places orders
admin --> myntraClone : Manages inventory and orders
myntraClone --> externalPaymentGateway : Processes payments
myntraClone --> deliveryPartner : Coordinates deliveries
myntraClone --> notificationService : Sends notifications
@enduml
