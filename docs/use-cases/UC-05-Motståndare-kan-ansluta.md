# UC-05-Motståndare-kan-ansluta

| Fält | Värde |
| **UC-ID** | 05 |
| **Aktör** | Motståndare |
| **Tillhörande krav** | IFK-01 |

#### Description
- Motståndare som tar emot inbjudan kan ansluta till parti

#### Precondition
- Motståndare har tagit emot en inbjudan

#### Trigger
- Motståndare accepterar inbjudan

#### Main flow
- Motståndare blir informerad om inbjudan
- Motståndare kan acceptera inbjudan
- Motståndare laddar in i spelet vid accepterad inbjudan

#### Postcondition
- Mottagen inbjudan kan användas för att ansluta
- Vid accepterad inbjudan ansluts motståndare till spelare

#### Alternative flow 01 - Inbjudan nekas
1. Motståndare tar emot inbjudan
2. Motståndare godkänner ej inbjudan
3. Spelare väntar i lobby
4. Parti startas ej

#### Alternative flow 02 - Inbjudan accepteras för sent
1. Motståndare godkänner inbjudan
2. Spelare är inte tillgänglig för att påbörja ett parti
3. Motståndare blir informerad
