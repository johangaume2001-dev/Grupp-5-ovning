# Begreppsmodell – Gomoku

*Mermaid kod genererad baserad på spelets flöde.
Begrepp använda från Glossary, taget från krav + diverse UC*

Denna begreppsmodell visar aktörer och begrepp i Gomoku, samt hur de relatrerar.
För tydligare förklaring gällande begreppen så kika på [våran Glossary :)](00-Glossary.md) 

```mermaid
classDiagram
    class Spelare {
        +spelarId
        +användarnamn
        +email
    }

    class Konto {
        +kontoId
        +lösenordHash
        +skapadDatum
    }

    class Samtycke {
        +samtyckeId
        +status
        +datum
    }

    class Parti {
        +partiId
        +status
        +resultat
    }

    class Spelbräda {
        +storlek
        +tillstånd
    }

    class Drag {
        +position
        +tidsstämpel
    }

    class Sten {
        +färg
        +position
    }

    class Session {
        +sessionId
        +status
    }

    class Inbjudan {
        +inbjudanId
        +status
    }

    class Speldata {
        +speldataId
        +krypteradData
        +lagringsdatum
    }

    Spelare "1" --> "0..1" Konto : har
    Konto "1" --> "0..1" Samtycke : kopplat till
    Spelare "2" --> "0..*" Parti : deltar i
    Spelare "1" --> "0..*" Inbjudan : skickar
    Inbjudan "1" --> "1" Session : skapar
    Session "1" --> "1" Parti : hör till
    Parti "1" --> "1" Spelbräda : har
    Spelbräda "1" --> "0..*" Sten : innehåller
    Parti "1" --> "0..*" Drag : består av
    Drag "0..*" --> "1" Spelare : utförs av
    Drag "1" --> "0..1" Sten : placerar
    Parti "1" --> "0..1" Speldata : genererar
```

## Kommentarer till modellen

- **Spelare –> Konto:** en spelare kan delta anonymt/gäst i vissa flöden, men behöver ett konto för att spara framsteg (kopplat till FK-09).
- **Spelare –> Parti:** varje parti kräver exakt två deltagare (FK-01, FK-05), medan en spelare kan delta i flera partier över tid.
- **Inbjudan –> Session:** en inbjudan resulterar i en session som motståndaren kan gå med i (FK-04, FK-05).
- **Parti –> Speldata:** speldata genereras och lagras säkert enligt GDPR när partiet spelas eller avslutas (FK-07, IFK-06).
- **Drag –> Spelare:** varje drag kopplas till den spelare som utförde det, och valideras mot spelets regler innan det godkänns (FK-08, IFK-05).
- **Konto –> Samtycke:** krävs för att hantera GDPR-relaterade krav som återkallande av samtycke och dataportabilitet (IFK-07, IFK-08, IFK-09).
.
