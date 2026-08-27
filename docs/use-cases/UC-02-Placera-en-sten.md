# UC-02-Placera-en-sten

| Fält | Värde |
|---|---|
| **UC-ID** | 02 |
| **Aktör** | Spelare |
| **Tillhörande krav** | FK-02 |

##### Description
- Spelare ska kunna placera en sten på tom ruta.

##### Precondition
- Spelare deltar i ett spel
- Det är spelarens tur

##### Trigger
- Spelare gör val av ruta där sten ska placeras

##### Mainflow 
1. Spelare klickar på ruta
2. Stenen placeras på vald ruta

##### Postconditions
- Stenen placerades korrekt på vald ruta


##### Alternative flow 01 - Fel ruta
1. Spelare väljer en ruta som är upptagen
2. System informerar spelare och nekar handlingen

##### Alternative flow 02 - Ej spelares tur
1. Spelare väljer ruta under motståndares tur
2. System informerar spelare och nekar handlingen
