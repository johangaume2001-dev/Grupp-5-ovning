
# UC‑16 – Bevara speldata (GDPR – lagring)

| Fält | Värde |
|---|---|
| **UC-ID** | 16 |
| **Aktör** | System (sekundär: användare) |
| **Tillhörande krav** | NFR‑16 |

### Description
Systemet lagrar speldata på ett säkert och korrekt sätt enligt GDPR.

### Pre-condition
- Användaren är inloggad
- Systemet har mottagit speldata
- Samtycke finns

### Trigger
- Systemet tar emot ny speldata under spelets gång

### Mainflow
1. Användaren genererar speldata genom att spela
2. Systemet tar emot speldata
3. Systemet kontrollerar att datan är korrekt
4. Systemet krypterar känslig spelinformation
5. Systemet lagrar speldata säkert
6. Systemet begränsar åtkomst till behöriga
7. Systemet loggar lagringshändelsen
8. Systemet visar bekräftelse

### Alternativflöde
A1 – Felaktig speldata: Systemet visar felmeddelande
A2 – Ingen rättslig grund: Systemet sparar inte speldata

### Undantag
- Tekniskt fel
- Krypteringsfel

