# Sequence Diagram Functie Aan Roepen

Hier wordt een sequentiediagram getoond waarin een functie-aanroep door een van de taken wordt geïllustreerd. Deze functie wordt opgeroepen om het knipperen van een lamp te regelen als signaal dat de bus klaar is om af te vuren. Het diagram toont de timing en volgorde van de functies en hoe deze bijdragen aan het procesbeheer.

```plantuml
@startuml

participant BusTask #red
participant Timer #grey
participant GVL_Carbid #green

BusTask -> GVL_Carbid : VoegCarbidToe
GVL_Carbid -> Timer : Start 2s delay
Timer --> GVL_Carbid : CarbidAdded == TRUE

BusTask -> GVL_Carbid : VoegWaterToe
GVL_Carbid -> Timer : Start 2s delay
Timer --> GVL_Carbid : WaterAdded == TRUE

BusTask -> GVL_Carbid : StartGasVorming
GVL_Carbid -> Timer : Start 10s delay
Timer --> GVL_Carbid : EnoughGas == TRUE

BusTask -> GVL_Carbid : ReadyToFire == TRUE
@enduml
```