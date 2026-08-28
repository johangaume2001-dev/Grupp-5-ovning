# UC-14-Fusk-skydd

| Fält | Värde |
| --- | --- |
| **UC-ID** | 15 |
| **Aktör** | Spelare |
| **Tillhörande krav** | IFK-06 |

#### Description
- Systemet ska kontrollera på serversidan att varje drag är giltigt och följer spelets regler.


### Pre-condition
- En match är aktiv.
- Spelaren deltar i matchen.
- Det är spelarens tur.

#### Trigger
- Spelaren skickar ett drag till servern.

#### Mainflow
1. Spelaren väljer en position på spelbrädan. 
2. Klienten skickar draget till servern.
3. Servern kontrollerar att draget följer spelets regler.
4. Servern kontrollerar att positionen är giltig och ledig.
5. Servern godkänner draget.
6. Servern uppdaterar spelbrädan.
7. Servern skickar den uppdaterade spelbrädan.

#### Postconditions
- Endast giltiga drag accepteras.
- Spelbrädan uppdateras endast efter att servern har godkänt draget.
- Spelets regler kan inte kringgås genom klienten.

#### Alternative flow 01 - Ogiltig position
1. Spelaren skickar ett drag med en ogiltig position.
2. Servern tar emot draget.
3. Servern kontrollerar positionen.
4. Servern konstaterar att positionen är ogiltig.
5. Servern avvisar draget.
6. Spelbrädet ändras inte.

#### Alternative flow 02 - Position redan upptagen
1. Spelaren skickar ett drag till en position som redan innehåller en sten.
2. Servern kontrollerar spelbrädet.
3. Servern konstaterar att positionen redan är upptagen.
4. Servern avvisar draget.
5. Spelbrädet ändras inte.

#### Alternative flow 03 - Fel spelares tur
1. En spelare skickar ett drag trots att det inte är spelarens tur.
2. Servern kontrollerar aktuell spelare.
3. Servern konstaterar att spelaren inte får göra ett drag.
4. Servern avvisar draget.
5. Spelbrädet ändras inte.

#### Alternative flow 04 - Manipulerat drag
1. Spelaren manipulerar klientens request.
2. Det manipulerade draget skickas till servern.
3. Servern validerar draget mot det aktuella spelbrädet och spelets regler.
4. Servern konstaterar att draget är ogiltigt.
5. Servern avvisar draget.
6. Spelbrädet ändras inte.
