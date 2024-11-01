# Inleiding

Dit project omvat de ontwikkeling van een PLC-programma dat het proces van carbidschieten simuleert. Hierbij worden carbid en water bij elkaar toegevoegd waardoor gasvorming ontstaat, wanneer hierbij een vlam wordt gehouden ontstaat er een harde knal. Dit programma automatiseert het volledige proces in gestructureerde stappen.

Het programma is geschreven in Structured Text en bevat twee onafhankelijke taken die communiceren via een Global Variable List (GVL). De taken voeren processen uit zoals het toevoegen van carbid en water, het plaatsen van de bal, en het afvuren tijdens het toevoegen van een vlam. Deze communicatie wordt verder inzichtelijk gemaakt door middel van state- en sequence-diagrammen die te zien zijn in de volgende hoofdstukken.

Voor versiebeheer en documentatie is een GitHub-repository opgezet. De code en documentatie zijn te vinden op mijn GitHub: [GitHub Repository Link](https://github.com/JoostPeters14/Carbid_Programma.git).

In de volgende hoofdstukken worden de opzet en werking van elke taak verder toegelicht met ondersteunende diagrammen en beschrijvingen.