# UC-07-Spara-spelets-tillstånd

| Fält | Värde |
|---|---|
|**UC-ID**| 07 |
|**Aktör**| Systemet |
|**Tillhörande krav**| **FK** |

##### Description
- Systemet sparar spelets tillstånd så att spelaren kan fortsätta senare

##### Preconditions
- Ett parti pågår

##### Trigger
- Spelaren gör ett giltigt drag

#### Mainflow
1. Spelaren gör ett giltigt drag.
2. Systemet sparar brädets aktuella tillstånd, turordning och speldata.

#### Postconditions
1. Det senaste spelläget är sparat och kan återställas.

#### Alternative flow 01 - Sparningen misslyckas
- Systemet informerar spelaren om att framsteg kan gå förlorat, och försöker spara igen
