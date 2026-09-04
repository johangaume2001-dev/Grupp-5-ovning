# UC-20-Spela-Rankad-Match

| Fält                 | Värde   |
| --------------------- | ------- |
| **UC-ID**              | 21      |
| **Aktör**              | Spelare |
| **Tillhörande krav**   | IFK-10  |

##### Description

- Spelaren spelar sin första rankade match mot en motståndare.

##### Pre-condition

- Spelare har ett registrerat konto
- Spelare befinner sig inte redan i en aktiv match

##### Trigger

- Spelare väljer att söka rankad match

##### Mainflow

1. Spelare väljer alternativ för att söka rankad match
2. Systemet placerar spelare i kö
3. Systemet matchar spelare med liknande rank/skicklighet
4. Matchen laddas in och partiet startar
5. Spelare och motståndare spelar partiet
6. Systemet beräknar resultat och uppdaterar rankingpoäng

##### Postconditions

- Matchens resultat är sparat
- Spelarens rankingpoäng är uppdaterad
- Spelare har en synlig ranking

#### Alternative flow 01 - Ingen motståndare hittas

1. Spelare väntar i matchningskön
2. Ingen lämplig motståndare hittas inom tidsgränsen
3. System meddelar spelare och avbryter sökningen

#### Alternative flow 02 - Spelare avbryter matchning

1. Spelare väljer att avbryta sökningen
2. Systemet tar bort spelare ur kön
3. Ingen match skapas
