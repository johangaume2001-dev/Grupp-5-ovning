# UC-08-Hantera-oglitiga-drag

| Fält | Värde |
|---|---|
|**UC-ID**| 08 |
|**Aktör**| Systemet |
|**Tillhörande krav** | IFK-07 |

#### Description
- Systemet stoppar drag som bryter mot spelreglerna och informerar spelaren om varför

#### Precondition
- Ett parti pågår.

#### Trigger
- Spelaren försöker göra ett drag.

#### Mainflow
1. Spelaren väljer en ruta för sitt drag.
2. Systemet kontrollerar att rutan är inom brädets gränser och ledig.
3. Systemet accepterar draget och placerar markeringen.

#### Postconditions
- Endast giltiga drag registreras på brädet.

#### Alternative flow 01 - Rutan är upptagen
- Systemet avvisar draget och visar felmeddelande "Rutan är redan upptagen".

#### Alternative flow 02 - Fel spelares tur
- Systemet avvisar draget och informerar om att det inte är spelarens tur.

#### Alternative flow 03 - Partiet är redan avslutat
- Systemet avvisar draget och erbjuder att starta ett nytt parti.

