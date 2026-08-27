# UC‑19 – Hantera samtycke för speldata (GDPR – samtyckeshantering)

| Fält | Värde |
|---|---|
| **UC-ID** | 19 |
| **Aktör** | Användare |
| **Tillhörande krav** | NFR‑19 |

### Description
Användaren ger, uppdaterar eller återkallar samtycke för hur speldata får behandlas enligt GDPR.

### Pre-condition
- Användaren är inloggad
- Systemet har en samtyckesmodul

### Trigger
- Användaren öppnar “Samtyckesinställningar”

### Mainflow
1. Användaren öppnar sidan för samtycke
2. Systemet hämtar aktuellt samtycke
3. Användaren väljer att ge, ändra eller återkalla samtycke
4. Systemet uppdaterar samtyckesstatus
5. Systemet sparar ändringen i loggar
6. Systemet visar bekräftelse

### Alternativflöde
A1 – Systemet kan inte hämta samtycke: Felmeddelande visas  
A2 – Användaren försöker återkalla samtycke som krävs för tjänsten: Systemet informerar om begränsningar

### Undantag
- Tekniskt fel vid uppdatering av samtycke

