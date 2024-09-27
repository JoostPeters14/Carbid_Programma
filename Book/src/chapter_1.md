# Chapter 1

```plantuml
@startuml
actor "Gebruiker" as user #yellow
participant "Carbidbus" as bus
participant "Water" as water #blue
participant "Carbid" as carbid #gray
participant "Bal" as bal #orange
'participant "Aansteker" as aansteker #red

user -> bus : Verwijder resten van eerder schot
user -> carbid : Voeg nieuw carbid toe
carbid -> user : Carbid is toegevoegd
user -> water : Voeg water toe aan bus
water -> carbid : Reageert met carbid
carbid -> bus : Gasvorming
carbid -> user : Genoeg water toegevoegd
user -> bus : Plaats bal in bus
bal -> bus : Bal sluit bus luchtdicht af
user -> bus : Houdt vlam bij bus
bus -> carbid : Carbid ontsteekt
carbid -> bal : Bal wordt weg geschoten 
carbid -> user : Harde knal hoorbaar
user -> bus : Controleer bus na schot
user -> bal : Haal bal op

@enduml