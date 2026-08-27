# UC‑20 – Placera markering (avancerad spelinteraktion)

| Fält | Värde |
|---|---|
| **UC-ID** | 20 |
| **Aktör** | Användare |
| **Tillhörande krav** | FR‑20 |

### Description
Användaren placerar en avancerad markering på spelplanen med utökad funktionalitet (t.ex. riktning, färg, typ).

### Pre-condition
- Användaren är inloggad
- Spelplanen är aktiv
- Systemet kan ta emot markeringar

### Trigger
- Användaren klickar på en position på spelplanen

### Mainflow
1. Användaren väljer en position på spelplanen
2. Systemet registrerar klicket
3. Användaren väljer typ av markering (t.ex. pil, cirkel, färg)
4. Systemet visar en förhandsvisning
5. Användaren bekräftar placeringen
6. Systemet placerar markeringen
7. Systemet uppdaterar spelplanen
8. Systemet loggar händelsen

### Alternativflöde
A1 – Ogiltig position: Systemet visar felmeddelande  
A2 – Markeringstyp saknas: Systemet ber användaren välja typ

### Undantag
- Tekniskt fel vid rendering  
- Markeringen kan inte sparas

