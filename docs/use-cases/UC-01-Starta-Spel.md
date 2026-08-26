# UC-01-Starta-Spel

| Fält | Värde |
|---|---|
|**UC-ID** | 01 |
| **Aktör** | Spelare |
| **Tillhörande krav* | FK-01 |

##### Description 
- Spelaren startar ett nytt parti.

##### Pre-condition
- Spelare har en motståndare
- Spelare deltar inte i ett aktivt parti

##### Trigger
- Spelare väljer alternativ för att påbörja nytt spel

##### Mainflow
 1. Spelare väljer alternativ för att starta nytt parti
 2. En tom bräda visas
 3. Ena deltagaren kan placera en sten på brädan.

##### Postconditions
- När spelare initierar nytt spel så skapas ett nytt parti
- Spelbrädan skall påbörjas tom
- Spelare och motståndare kan delta



### Alternative flow 01 - Saknat motstånd
 1. Spelare har inte valt motståndare.
 2. Spelare försöker starta nytt parti
 3. System meddelar spelare

### Alternative flow 02 - Online match laddas ej
 1. Spelare har valt en motståndare
 2. Motståndare laddar ej in i matchen
 3. Spelare får felmeddelande
