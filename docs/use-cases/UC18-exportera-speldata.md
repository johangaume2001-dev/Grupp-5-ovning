# UC‑18 – Exportera speldata (GDPR – dataportabilitet)

| Fält | Värde |
|---|---|
| **UC-ID** | 18 |
| **Aktör** | Användare |
| **Tillhörande krav** | NFR‑18 |

### Description
Användaren exporterar all speldata i ett läsbart och standardiserat format (JSON/CSV) enligt GDPR:s krav på dataportabilitet.

### Pre-condition
- Användaren är inloggad
- Systemet har lagrad speldata

### Trigger
- Användaren klickar på “Exportera speldata”

### Mainflow
1. Användaren begär export av speldata
2. Systemet tar emot begäran
3. Systemet verifierar användarens identitet
4. Systemet hämtar all speldata kopplad till användaren
5. Systemet paketerar speldata i ett standardformat (JSON/CSV)
6. Systemet gör filen tillgänglig för nedladdning
7. Systemet visar bekräftelse på att exporten är klar

### Alternativflöde
A1 – Identiteten kan inte verifieras: Systemet avbryter exporten  
A2 – Ingen speldata finns: Systemet visar “Ingen speldata att exportera”

### Undantag
- Tekniskt fel vid export

