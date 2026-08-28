# UC‑17 – Radera speldata (GDPR – rätt att bli raderad)

| Fält | Värde |
|---|---|
| **UC-ID** | 17 |
| **Aktör** | Användare (sekundär: system) |
| **Tillhörande krav** | NFR‑17 |

### Description
Användaren raderar all speldata kopplad till sitt konto enligt GDPR Artikel 17.

### Pre-condition
- Användaren är inloggad
- Systemet har lagrad speldata

### Trigger
- Användaren klickar på “Radera speldata”

### Mainflow
1. Användaren begär radering av speldata
2. Systemet tar emot begäran
3. Systemet verifierar användarens identitet
4. Systemet markerar speldata för radering
5. Systemet raderar speldata från databasen
6. Systemet raderar loggar som innehåller speldata
7. Systemet visar bekräftelse på radering

### Alternativflöde
A1 – Identiteten kan inte verifieras: Systemet avbryter och visar felmeddelande  
A2 – Speldata behövs för rättslig skyldighet: Systemet informerar att radering inte kan utföras

### Undantag
- Tekniskt fel vid radering

