# Glossary – Gomoku

*Detta dokument samlar de centrala begreppen i Gomoku-projektet. 
Termerna är hämtade från alla krav och användningsfall. 
Syftet är att alla ska ha en gemensam förståelse av vad varje ord betyder i just detta system.*

## Termer

| Term | Definition |
| --- | --- |
| **Spelare** | En användare som deltar i ett parti och kan påbörja spel, placera stenar, avsluta ett parti i förväg eller bjuda in en vän. |
| **Motståndare** | Den andra deltagaren i ett parti, som kan gå med i en session skapad av en spelare. |
| **Parti** | Ett enskilt spelomgång/match mellan två deltagare, från start till att spelet avslutas (vinst, förlust eller kapitulation). |
| **Spelbräda** | Rutnätet som ett parti spelas på. Skapas tomt när ett nytt parti startas. |
| **Sten** | Den spelpjäs en spelare placerar på spelbrädan under sin tur. |
| **Drag** | En spelares handling att placera en sten på en specifik position på brädan. |
| **Ogiltigt drag** | Ett drag som bryter mot spelets regler (t.ex. position redan upptagen eller utanför brädan) och som systemet ska avvisa. |
| **Session** | Den aktiva spelomgången som kopplar ihop två deltagare i realtid, t.ex. via en inbjudningslänk. |
| **Inbjudan** | En förfrågan en spelare skickar till en vän för att denne ska kunna gå med i spelarens session. |
| **Deltagare** | Samlingsbegrepp för spelare och motståndare i ett aktivt parti. Endast deltagare ska ha åtkomst till partiet. |
| **Vinst/Vinstvillkor** | Det tillstånd då en spelare har fem stenar i rad (horisontellt, vertikalt eller diagonalt) och partiet avgörs. Systemet ska förmedla vinsten korrekt. |
| **Spelets tillstånd** | Den fullständiga informationen om ett pågående parti (brädans innehåll, vems tur det är, status) som systemet kan spara. |
| **Konto** | En registrerad identitet i systemet kopplad till en spelare, används för inloggning och för att spara framsteg. |
| **Registrering** | Processen där en spelare skapar ett konto genom att ange e-post, användarnamn och lösenord. |
| **Inloggning** | Processen där en spelare autentiserar sig med sina kontouppgifter. |
| **Kontolåsning** | Säkerhetsåtgärd där ett konto låses efter ett antal felaktiga inloggningsförsök. |
| **Klient** | Applikationen (t.ex. webbläsare eller app) som spelaren använder för att skicka förfrågningar (requests) till systemet. |
| **Request** | En förfrågan som skickas från klienten till systemet, t.ex. för att utföra ett drag. Ska alltid valideras serverside så att ogiltiga drag inte kan skickas in. |
| **Rate-limiting** | Teknik för att begränsa antalet anrop från en klient under en viss tid, så att systemet inte kan överbelastas via massanrop. |
| **Regelvalidering** | Systemets kontroll av att ett drag följer spelets regler innan det godkänns. |
| **Speldata** | Data som genereras under ett parti (drag, resultat, tidsstämplar m.m.) som systemet lagrar säkert. |
| **Personuppgifter** | Information som kan identifiera en spelare (t.ex. e-post, användarnamn), vilka ska skyddas enligt GDPR. |
| **GDPR** | EU:s dataskyddsförordning som styr hur personuppgifter och speldata får samlas in, lagras och hanteras. |
| **Samtycke** | Spelarens godkännande till att systemet får behandla dennes personuppgifter/speldata. Kan återkallas av spelaren. |
| **Kryptering** | Metod för att skydda känslig speldata och personuppgifter vid lagring. |
| **Dataportabilitet** | Spelarens rättighet enligt GDPR att få ut sin data i ett strukturerat, maskinläsbart format. |
| **Rätt att bli glömd** | Spelarens rättighet att radera all data kopplad till sitt konto. |
| **Åtkomstkontroll** | Mekanism som säkerställer att endast behöriga (t.ex. deltagare i ett aktivt parti) har tillgång till viss data eller funktionalitet. |
| **FK (Funktionellt krav)** | Ett krav som beskriver vad systemet ska göra, t.ex. "Spelare ska kunna placera en sten" (FK-02). |
| **IFK/NFR (Icke-funktionellt krav)** | Ett krav som beskriver hur systemet ska bete sig, t.ex. prestanda, säkerhet eller efterlevnad av GDPR (t.ex. IFK-06). |
| **Use case** | En dokumenterad beskrivning av hur en aktör interagerar med systemet för att uppnå ett mål, inklusive för- och eftervillkor samt flöden. |

