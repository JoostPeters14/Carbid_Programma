# Sequence Diagram Tussen Tasks

Dit hoofdstuk bevat een sequentiediagram waarin de communicatie tussen de UserTask en BusTask wordt weergegeven. Hierin wordt gedetailleerd beschreven hoe de twee taken via variabelen in de GVL samenwerken en informatie uitwisselen om de toestand van het proces correct te beheren.

```plantuml
@startuml
actor Gebruiker #yellow
participant UserTask #blue
participant BusTask #red

Gebruiker -> UserTask : StartProcess
UserTask -> BusTask : AddCarbid
BusTask -> UserTask : CarbidAdded

UserTask -> BusTask : AddWater
BusTask -> UserTask : WaterAdded

UserTask -> BusTask : BallPlaced
BusTask -> UserTask : ReadyToFire

Gebruiker -> UserTask : FlameOn
UserTask -> BusTask : Fire
BusTask -> UserTask : Fire == TRUE

UserTask -> BusTask : Reset
@enduml
```