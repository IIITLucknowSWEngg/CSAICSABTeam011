<img src="https://www.plantuml.com/plantuml/png/TPBDRjj038JlVWhM9nVmpwMddf8wGLkWBeJAFGUqH5iBx8_0fUpexSkLDh3Yk9T49fOVEJDyY88idREpJyPNjgi96f4sVjri62_hav6cEtIHk0fUoCkw2cxJMlIfPnMbjkQmsNvP5QdqT_Thup0AiPPUjgdZLTPjei_4Y2NOzLuOOMk39rX1sUjZ1_abF1ayCRhPh22EmI-gBafmn4kOR_FdNB-VVGrf9RWq0GuSBf4Ye1RRZgi6qw-MGzrL4jVppsymh9tnslsO_YVC3ZsUhc_1-BCA3Dml8N2jJSi16bfY51Fy09kDAo_S86JGeQYfh8H-1BL8Ze4Tw1y8tXfF49lGjiQV9foNvrTPg7HYZxR0tf6NxoXqmLunkG2vaiZxnd2zQf6bXpYw9o59g2YgbB4XRJeTK9CrP-A-q3O_sFcKAv1BEOd1tRmDHEApgMXGu99NkZfabA7R6Jw8EPfgSAeSEnNsUrA5NBwLCPqJoTTf33aqLWCeT-KoHniRcCp8QVmXExcIzw5y6ozZgL3Kkw2OIHRLgnmnT577AKb1-K9kAFbAxbz7liCQ1U5iy6sZTuJ_fpk6HjVOG1eEtQb93ltOxujIWHzu7yFSXi3gceBZ99-qq72BnSzxcFjvbUf_zWQgu8-6tUZsABPLfPHDkx8VjAbpzXy0" alt="Myntra Clone - System Context Diagram">

```plantuml
@startuml
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Context.puml

title Myntra Clone - System Context Diagram

Person(customer, "Customer", "End user who browses and purchases products.")
Person(admin, "Admin", "Manages product inventory, orders, and operations.")

System(myntraClone, "Myntra Clone", "A platform for online shopping.")

System_Ext(externalPaymentGateway, "Payment Gateway", "Third-party system to process payments.")
System_Ext(deliveryPartner, "Delivery Partner System", "External service for managing deliveries.")
System_Ext(notificationService, "Notification Service", "Third-party service for sending emails, SMS, and push notifications.")

Rel(customer, myntraClone, "Browses, searches, and places orders using")
Rel(admin, myntraClone, "Manages inventory, orders, and user data via")

Rel(myntraClone, externalPaymentGateway, "Processes payments through", "HTTPS")
Rel(myntraClone, deliveryPartner, "Coordinates deliveries via", "API")
Rel(myntraClone, notificationService, "Sends order confirmations and updates using", "API")

@enduml
