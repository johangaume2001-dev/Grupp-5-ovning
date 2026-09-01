# UC-10-Låsa-konto-vid-för-många-felaktiga-försök

| Fält | Värde |
|---|---|
| **UC-ID** | 10 |
| **Aktör** | Spelare |
| **Tillhörande krav** | IFK10 |

#### Description
- Systemet låser ett konto tillfälligt när för många felaktiga inloggningsförsök har gjorts i följd, för att skydda kontot mot obehörig åtkomst.

#### Precondition
1. Kontot existerar och är inte redan låst.
2. Spelaren försöker logga in.

#### Trigger
- Spelaren anger fel lösenord ett antal gånger i följd (t.ex försök). 

#### Mainflow
1. Spelaren anger e-post/användarnamn och lösenord.
2. Systemet kontrollerar uppgifterna och finner att lösenordet är felaktigt.
3. Systemet räknar upp antalet misslyckade försök för kontot. 
4. Systemet jämför antalet försök mot den tillåtna gränsen.
5. Antalet misslyckade försök når gränsen.
6. Systemet låser kontot.
7. Systemet informerar spelaren om att kontot är låst och varför.

#### Postconditions
1. Kontot är markerat som låst.
2. Spelaren kan inte logga in, även med korrekt lösenord, förrän kontot låses upp.

#### Alternative flow 1 - Spelaren loggar in korrekt innan gränsen nås
- Räknaren för felaktiga försök återställs till noll.

#### Alternative flow 2 - Spelaren försöker logga in på ett redan låst konto
- Systemet avvisar försöket direkt och informerar om att kontot är låst, utan att räkna det som ytterligare ett misslyckat försök. 

#### Alternative flow 3 - Spelaren vill låsa upp kontot
- Systemet erbjuder t.ex. återställning av lösenord eller en tidsbaserad automatisk upplåsning.

