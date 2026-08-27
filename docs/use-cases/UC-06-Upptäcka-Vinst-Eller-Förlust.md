| Fält | Värde |
|---|---|
|**UC-ID** | 06 |
|**Aktör** | Systemet |
|**Tillhörande krav** | **FK** |

##### Description
- Systemet avgör automatiskt spelets utfall efter varje drag.

##### Precondition
- Ett parti pågår.
- Ett giltigt drag har precis gjorts.

##### Trigger
- Ett nytt, glitigt drag registreras av systemet.

##### Mainflow
1. Systemet tar emot det nya draget.
2. Systemet kontrollerar brädet i alla riktningar (rad, kolumn, diagonaler) från den nya markeringen.
3. Systemet hittar fem markeringar i rad av samma spelare. 
4. Systemet markerar partiet som avslutat med vinnare.
5. Systemet visar resultatet för båda spelarna. 

##### Postconditions
- Partiets status är satt till "avslutat".
- Resultatet är synligt för båda spelare. 

##### Alternative flow 01 - Brädet är fullt utan vinnare
- Systemet markerar partiet som oavgjort och meddelar båda spelarna.

##### Alternative flow 02 - Inget femtal och brädet är inte fullt
- Systemet fortsätter partiet, turen växlar som vanligt. 
