# **09. Affärsregler**

Detta dokuemnt beskriver affärsregler för Gomoku systemet. Regler och begränsningar som gäller övergripande i systemet snarare än inom ett specifikt use case. Affärsreglerna kompletterar de funktionella kraven genom att definiera de policys och gränser som systemet alltid måste följa.

## AR-01: Spelregler

| ID | Regel |
|---|---|
| AR-01.1 | Spelbrädet ska vara 15x15 rutor. |
| AR-01.2 | Två spelare deltar i ett parti, en med svart markeringar och en med vita. |
| AR-01.3 | Spelare växlar drag, en markering placeras per tur. |
| AR-01.4 | En markering kan endast placeras på en ledig ruta. |
| AR-01.5 | Markeringar får varken flyttas eller tas bort under spelets gång. |
| AR-01.6 | Spelaren med fem i rad alltid partiet. |
| AR-01.7 | Om brädet fylls helt utan att någon av spelarna uppnått fem i rad blir partiet oavgjort |

## AR-02: Tidsbegränsningar

| ID | Regel |
|---|---|
| AR-02.1 | Varje spelare har en maximal tid på sig att göra ett drag, t.ex 60 sekunder. |
| AR-02.2 | Om tiden går ut förlorar spelaren automatiskt paritet. |
| AR-02.3 | Tidsgränser kan konfigureras av systemadministratören |

## AR-03: Spelkonton och identitet

| ID | Regel |
|---|---|
| AR-03.1 | Endast registrerade användare får spela rankade matcher. |
| AR-03.2 | Gästspelare får spela orankade matcher men deras resultat sparas inte långsiktigt. |
| AR-03.3 | Användare måste acceptera användarvillkor innan de kan spela online. |

## AR-04: Poäng, ranking och historik

| ID | Regel |
|---|---|
| AR-04.1 | Vinst ger +3 poäng, oavgjort +1 poäng, förlust -2 poäng. |
| AR-04.2 | Ranking beräknas baserat på poäng över tid. |
| AR-04.3 | Matchhistorik (motståndare, datum, resultat) sparas i databasen. |

## AR-05: AI-motståndare

| ID | Regel |
|---|---|
| AR-05.1 | AI spelar alltid enligt samma spelregler som mänskliga spelare. |
| AR-05.2 | Svårighetsgrad styr hur långt AI analyserar framtida drag. |
| AR-05.3 | AI får inte använda otillåtna genvägar (t.ex manipulera brädet direkt). |

## AR-06: Fair play och fusk

| ID | Regel |
|---|---|
| AR-06.1 | Manipulation av klienten eller nätverkstrafik för att ändra spelresultat är förbjudet. |
| AR-06.2 | Systemet ska logga misstänkta beteenden som t.ex omöjliga drag. |
| AR-06.3 | Konton som bryter mot regler kan spärras av administratör. |

## AR-07: Integritet och GDPR

| ID | Regel |
|---|---|
| AR-07.1 | Personuppgifter får endast användas för spelrelaterade funktioner (konto, ranking, historik). || AR-07.2 | Användare ska kunna begära radering av sitt konto och sina personuppgifter. |
| AR-07.3 | Cookie-baserad tracking får inte aktiveras innan användaren gett samtycke. |
