# UC-14-Åtkomstkontroll

| Fält | Värde |
| --- | --- |
| **UC-ID** | 14 |
| **Aktör** | Spelare |
| **Tillhörande krav** | IFK-05 |

#### Description
- Endast spelare som är med i en match ska kunna göra drag.

### Pre-condition
- En match är aktiv.
- Spelaren är inloggad.
- Spelaren försöker göra ett drag i en match.

#### Trigger
- Spelaren skickar ett drag till servern.

#### Mainflow
1. Spelaren skickar ett drag till servern.
2. Servern identifierar spelaren.
3. Servern kontrollerar att spelaren tillhör den aktuella matchen.
4. Servern kontrollerar att det är spelarens tur.
5. Servern godkänner draget.
6. Servern uppdaterar spelbrädet.
7. Det uppdaterade spelbrädet skickas till matchens deltagare.

#### Postconditions
- Endast en spelare som deltar i matchen kan göra ett drag.
- Ett godkänt drag uppdaterar spelbrädet. 
- Spelare som inte deltar i matchen kan inte påvärka spelbrädan.

#### Alternative flow 01 - Spelaren tillhör inte matchen
1. En spelare skickar ett drag till servern.
2. Servern identifierar spelaren.
3. Servern kontrollerar spelarens deltagande i matchen.
4. Servern konstaterar att spelaren inte deltar i matchen.
5. Servern avvisar draget.
6. Spelbrädet ändras inte.
7. Spelaren får ett felmeddelande.

#### Alternative flow 02 - Manipulerad request
1. En spelare manipulerar en request och anger en match som spelaren inte deltar i.
2. Servern tar emot requesten.
3. Servern kontrollerar spelarens behörighet till matchen.
4. Servern konstaterar att spelaren inte tillhör matchen.
5. Servern Avvusar requesten.
6. Spelbrädan ändras inte.
