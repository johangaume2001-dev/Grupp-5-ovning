# UC-13-Rate-Limiting

| Fält | Värde |
| --- | --- |
| **UC-ID** | 13 |
| **Aktör** | Klient |
| **Tillhörande krav** | IFK-04 |

#### Description
- Systemet ska begränsa hur många request en klient får skicka under en viss tidsperiod. 

### Pre-condition
- Klienten är ansluten till systemet.
- Systemet har en definierad gräns för antal requests under en viss tidsperiod.

#### Trigger
Klienten skickar en request till systemet.

#### Mainflow
1. Klienten är ansluten till systemet.
2. Servern registrerar requesten.
3. Servern kontrollerar hur många requests har skickat under den aktuella tidsperioden.
4. Servern konstaterar att klienten inte har överskridit gränsen.
5. Servern behandlar requesten.
6. Servern Skickar ett svar till klienten

#### Postconditions
- Requesten har behandlats om klienten håller sig inom den tillåtna gränsen.
- Antalet requests från klienten har registrerats.

#### Alternative flow 01 - Rate limit överskrids
1. Klienten skickar en request till servern.
2. Servern kontrollerar antalet requests från klienten under den aktuella tidsperioden.
3. Servern konstaterar att klienten har överskridit den tillåtna gränsen.
4. Servern avvisar requesten.
5. Servern informerar klienten om att rate limit har överskridits.
6. Requesten behandlas inte.

#### Alternative flow 02 - Många requests skickas upprepade gånger
1. Klienten skickar flera requests inom en kort tidsperiod.
2. Servern registrerar requestsen.
3. Antalet requests överstiger den tillåtna gränsen.
4. Servern börjar avvisa ytterligare requests.
5. När tidsperioden har löpt ut kan klienten åter skicka requests inom den tillåtna gränsen.
