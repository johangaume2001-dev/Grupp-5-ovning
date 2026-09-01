# UC-09-Skapa-konto

|**Fält**|**Värde**|
|---|---|
|**Aktör**| Spelaren |
|**Tillhörande krav**| IFK-08 |

#### Description
- Spelaren ska kunna registrera sig för att spara framsteg och spela online.

#### Preconditions
1. Användaren har systemet öppet.
2. Användaren har inget befintligt konto.

#### Trigger
- Användaren trycker på "Skapa konto".

#### Mainflow

1. Användaren trycker skapa konto.
2. Systemet visar ett registreringsformulär (e-post, användarnamn, lösenord).
3. Användaren fyller i uppgifterna och bekräftar.
4. Systemet kontrollerar att e-postadressen inte redan är registrerad.
5. Systemet kontrollerar att lösenordet uppfyller kraven.
6. Systemet skapar kontot.
7. Systemet skickar ett bekräftelsemail till användaren. 

#### Postconditions
- Ett nytt konto finns registrerat i systemet.
- Användaren kan logga in med de angivna uppgifterna.

#### Alternative flow 1 - E-postadressen är redan registrerad
- Systemet avvisar registreringen och informerar användaren om att adressen redan är i bruk.

#### Alternative flow 2 - Lösenordet uppfyller inte kraven
- Systemet avvisar registreringen och visar vilka krav som saknas (t.ex minsta längd, specialtecken).

#### Alternative flow 3 - Obligatoriska fält är tomma
- Systemet avvisar registreringen och markerar vilka fält som saknas.
