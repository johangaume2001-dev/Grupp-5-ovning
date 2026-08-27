#UC-11-Manipulationsskydd

| Fält | Värde |
| --- | --- | 
| **UC-ID** | 11 |
| **Aktör** | Spelare |
| **Tillhörande krav** | IFK-02 |

#### Description
- En spelare ska inte kunna skicka ogiltigt drag genom att manipulera klientens request.

### Pre-condition
- Ett parti är aktivt.
- Spelarens tur.
- Det är spelarens tur.
- Spelaren har tillgång till spelets klient.

#### Trigger 
- Spelaren skickar ett drag till serven.

#### Mainflow
1. Spelaren väljer en position på spelbrädet.
2. Klienten skickar spelarens drag till servern.
3. Servern kontrollerar att draget är giltigt.
4. Servern kontrollerar att positionen är ledig.
5. Servern kontrollerar att det är spelarens tur.
6. Servern godkänner draget.
7. Servern uppdaterar spelbrädet.
8. Det uppdaterade spelbrädet skickas till spelarna.

#### Postconditions
- Endast giltiga drag accepteras.
- Spelbrädan innehåller inte ett manipulerat eller ogiltigt drag.
- Spelets tillstånd hanteras av servern.

#### Alternative flow 01 - Manipulerad position
1. Spelaren manipulerar klientens request och skickar en annan position än den som valts i klienten.
2. Servern tar emot requesten.
3. Servern kontrollerar om positionen är giltig.
4. Servern upptäcker att draget är ogiltigt.
5. Servern avvisar draget.
6. Spelbrädet ändras inte.
7. Spelaren får ett felmeddelande.

#### Alternative flow 02 - Drag på upptagen position
1. Spelaren manipulerar requesten och försöker placera en sten på en redan upptagen position.
2. Servern tar emot requesten.
3. Servern kontrollerar positionen mot det aktuella spelbrädet.
4. Servern upptäcker att positionen redan är upptagen.
5. Servern avvisar draget.
6. Spelbrädet ändras inte.

#### Alternative flow 03 - Felaktig spelares tur
1. Spelaren manipulerar requesten för att skicka ett drag trots att det inte är spelarens tur.
2. Servern tar emot requesten.
3. Servern kontrollerar vilken spelares tur det är.
4. Servern upptäcker att spelaren inte får göra draget.
5. Servern avvisar requesten.
6. Spelbrädt ändras inte.
