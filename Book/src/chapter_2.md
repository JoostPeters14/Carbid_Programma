# 2

```plantuml
@startuml
actor "PLC" as plc

rectangle "Extruder" {
    plc --> "Input: Start Signaal"
    plc <-- "Output: Starten"
    plc <-- "Output: Stoppen"
}

rectangle "Cutting Tool" {
    plc --> "Input: Reed Switch Open"
    plc <-- "Output: Snijtool Dicht"
}

rectangle "Grijper" {
    plc --> "Input: Fotocel Materiaal"
    plc <-- "Output: Pneumatisch In"
    plc <-- "Output: Pneumatisch Uit"
}

rectangle "Lengte Deegstreng Detectie" {
    plc --> "Input: Fotocel Lengte Deegstreng"
}

rectangle "Lopende Band" {
    plc <-- "Output: Start Band"
}

@enduml
