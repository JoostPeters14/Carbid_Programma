# State Diagrammen van de Taken
In dit hoofdstuk worden de statusdiagrammen van de afzonderlijke taken weergegeven. Hierin worden de stappen van elke taak in het proces van carbidschieten beschreven. De diagrammen helpen om de logische opbouw van de taken en de flow tussen verschillende processtappen te begrijpen.

# State Diagram UserTask

```plantuml
@startuml UserTask

skinparam backgroundcolor transparent

[*] -right-> Init : Power On
Init --> AddingCarbid : Start Process Triggered
AddingCarbid --> AddingWater : Carbid Added
AddingWater --> PlacingBall : Water Added
PlacingBall --> WaitingForFlame : Ball Placed
WaitingForFlame --> Firing : Flame Detected
Firing --> CheckingAfterShot : Fire Completed
CheckingAfterShot --> RetrievingBall : Check Complete
RetrievingBall --> Init : Ball Retrieved

state Init {
    Init : Initial state
}

state AddingCarbid {
    AddingCarbid : Adding carbid to bus
}

state AddingWater {
    AddingWater : Adding water to bus
}

state PlacingBall {
    PlacingBall : Placing ball in bus
}

state WaitingForFlame {
    WaitingForFlame : Waiting for flame to start firing
}

state Firing {
    Firing : Shooting the ball
}

state CheckingAfterShot {
    CheckingAfterShot : Checking bus after firing
}

state RetrievingBall {
    RetrievingBall : Retrieving the ball after firing
}

@enduml
```

# State Diagram BusTask

```plantuml
@startuml BusTask

skinparam backgroundcolor transparent

[*] -right-> WaitingForCarbid : Power On
WaitingForCarbid --> WaitingForWater : Carbid Added
WaitingForWater --> GasFormation : Water Added
GasFormation --> ReadyToFire : Enough Gas Formed
ReadyToFire --> Fired : Fire Triggered
Fired --> CleaningUp : Fire Completed
CleaningUp --> WaitingForCarbid : Cleanup Completed

state WaitingForCarbid {
    WaitingForCarbid : Awaiting carbid addition
}

state WaitingForWater {
    WaitingForWater : Awaiting water addition
}

state GasFormation {
    GasFormation : Gas is forming in bus
    GasFormation : Timed for 10 seconds
}

state ReadyToFire {
    ReadyToFire : Ready to fire, blinking indicator
}

state Fired {
    Fired : Firing the shot
}

state CleaningUp {
    CleaningUp : Removing debris
}

@enduml
```
