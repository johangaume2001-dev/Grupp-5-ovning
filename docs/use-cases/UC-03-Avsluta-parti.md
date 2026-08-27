# UC-03-Avsluta-Parti

| Fält | Värde |
|---|---|
| **UC-ID** | 03 |
| **Aktör** | Spelare |
| **Tillhörande krav** | FK-03 |

#### Description
Spelare kan avsluta ett pågående parti

#### Precondition
- Spelare deltar i ett aktivt parti

#### Trigger
- Spelare gör val för avsluta/ge upp

#### Main flow
1. Spelare vill avsulta spel
2. Spelare genomför val för forfeit
3. Parti avslutas med förlust

#### Postcondition
- Spelet pågår inte längre
- Resultatet blev förlust

### Alternative flow 01 - Spel redan avslutat
1. Spelare deltar i aktivt parti
2. Det är motståndares tur att spela
3. Motståndaren lägger en sten som resulterar i vinst
4. Spelare försöker samtidigt att kapitulera
5. System ignorerar "Avsluta" alternativ och motståndare vinner

