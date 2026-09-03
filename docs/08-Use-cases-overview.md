# 08 – Use‑cases Overview

## Syfte
Detta dokument ger en översikt över systemets användningsfall. Syftet är att beskriva vilka aktörer som interagerar med systemet och vilka huvudsakliga funktioner som stöds.

## Aktörer

### Spelaren
### Motspelaren (AI eller vän)
### Systemet som sparar spelet

---

## Översikt av användningsfall

| **UC‑ID** | **Namn**                        | **Beskrivning** |
|----------|----------------------------------|------------------|
| UC‑01 | Starta spel | Spelaren påbörjar ett nytt parti. |
| UC‑02 | Placera en sten | Spelaren placerar en sten på spelbrädet. |
| UC‑03 | Avsluta parti | Spelaren avslutar spelet i förväg. |
| UC‑04 | Bjuda in vän | Spelaren skickar en inbjudan till en vän. |
| UC‑05 | Motståndare kan ansluta | Motståndaren ansluter till spelarens spel. |
| UC‑06 | Upptäcka vinst, förlust eller oavgjort | Systemet avgör och visar resultatet. |
| UC‑07 | Spara spelets tillstånd | Systemet sparar spelets status för återupptagning. |
| UC‑08 | Hantera ogiltiga drag | Systemet validerar och avvisar felaktiga drag. |
| UC‑09 | Skapa konto | Spelaren skapar ett nytt konto. |
| UC‑10 | Låsa konto | Systemet låser kontot vid upprepade felinloggningar. |
| UC‑11 | Manipulationsskydd | Systemet förhindrar otillåtna ändringar i speldata. |
| UC‑12 | Integritet | Systemet skyddar användarens personuppgifter enligt GDPR. |
| UC‑13 | Rate‑limiting | Systemet begränsar antalet förfrågningar för att undvika överbelastning. |
| UC‑14 | Åtkomstkontroll | Endast behöriga användare får åtkomst till aktivt parti. |
| UC‑15 | Fusk‑skydd | Systemet upptäcker och förhindrar fusk under spelet. |
| UC‑16 | Bevara speldata | Systemet lagrar speldata säkert enligt GDPR. |
| UC‑17 | Radera speldata | Användaren kan radera all speldata kopplad till sitt konto. |
| UC‑18 | Exportera speldata | Användaren kan exportera speldata i läsbart format. |
| UC‑19 | Hantera samtycke för speldata | Användaren ger eller nekar samtycke för behandling av speldata. |
| UC‑20 | Placera markering i avancerat spelläge | Användaren placerar en markering med extra regler aktiverade. |

---

## Relationer mellan användningsfall
- UC‑01 måste ske innan UC‑02, UC‑03, UC‑04 och UC‑05.
- UC‑02 hänger ihop med UC‑08 (drag → validering).
- UC‑06 beror på UC‑02 (drag leder till vinst).
- UC‑07 triggas efter varje UC‑02.
- UC‑10–UC‑17 är kopplade till säkerhet och GDPR‑krav.
- UC‑19 måste ske innan UC‑16, UC‑17 och UC‑18 (samtycke → databehandling).
- UC‑20 är en utökning av UC‑02 (avancerat spelläge).

---

## Förutsättningar (Preconditions)
- Spelaren måste vara inloggad (om kontosystem finns).
- Ett spel måste vara startat innan drag kan göras.
- Motståndare kan endast gå med i en aktiv session.
- Samtycke (UC‑19) måste vara hanterat innan speldata får behandlas.

---

## Eftervillkor (Postconditions)
- Systemet uppdaterar spelstatus efter varje drag.
- Vid avslutat parti sparas slutresultatet.
- Vid vinst visas resultat
