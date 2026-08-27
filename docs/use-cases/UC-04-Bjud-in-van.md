# UC-04-Bjud-in-van

| Fält | Värde|
|---|---|
| **UC-ID** | 04 |
| **Aktör** | Spelare |
| **Tillhörande krav** | FK-04 |

#### Description
- Spelare ska kunna bjuda in vänner

#### Precondition
- Spelare har URL eller annan data som kan delas

#### Trigger
- Spelare väljer alternativ för att bjuda in en vän

#### Main flow
1. Spelare väljer motståndare
2. Spelare sparar nödvändig data
3. Spelare kan skicka data till motståndare
4. Motståndare kan ansluta till spelet
5. Nytt parti kan påbörjas

#### Postcondition
- Spelare kan välja motståndare
- Motståndare tog emot giltig inbjudan
- Motståndaren lyckas ansluta

### Alternative flow 01 - Lobby startas ej i tid
1. Spelare bjuder in en vän
2. Spelare stänger ner spel
3. Motståndare försöker ansluta
4. Motståndare får felmeddelande

