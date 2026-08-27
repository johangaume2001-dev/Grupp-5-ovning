# UC-12-Intergritet
| Fält | Värde |
| --- | --- |
| **UC-ID** | 12 |
| **Aktör** | Spelare |
| **Tillhörande krav** | IFK-03 |

##### Description
- Spelarens personuppgifter ska inte visas för andra spelare.

##### Pre-condition
- Spelaren är registrerad i systemet.
- Spelaren deltar i eller kan delta i ett parti.
- Det finns andra spelare som kan se spelarens information.

### Trigger 
- En spelare visar information om en annan spelare, exempelvis i samband med ett parti.

### Mainflow 
1. Spelaren startar eller deltar i ett parti
2. Systemet identifierar spelarna som deltar i partiet.
3. Systemet visar endast den information som andra spelare behöver för att delta i partiet.
4. Personuppgifter som inte behöver visas för andra spelare döljs.
5. Den andra spelaren kan fortsätta spela utan att få tillgång till dolda personuppgifter.

#### Postconditions
- Spelarens personuppgifter är inte synliga för andra spelare.
- Endast nödvändig spelarrelaterad information visas.
- Andra spelare kan inte få tillgång till dolda personuppgifter genom spelets gränssnitt.

#### Alternative flow 01 - Försök att visa dold information
1. En spelare försöker få fram en annan spelares personuppgifter.
2. Systemet kontrollerar om spelaren har rätt att se informationen.
3. Systemet konstaterar att informationen inte får visas.
4. Systemet nekar åtkomst.
5. Personuppgifterna visas inte för spelaren.

#### Alternative flow 02 - Manipulerad request
1. En spelare manipulerar en request för att försöka hämta en annan spelares personuppgifter.
2. Servern tar emot requesten. 
3. Servern kontrollerar spelarens behörighet.
4. Servern konstaterar att spelaren att spelaren saknar behörighet.
5. Servern returnerar inte de skyddade personuppgifterna.
6. Spelaren får endast tillgång tilll information som är tillåten att visa.
