```mermaid
flowchart TD
    T[Trigger: registrera/uppdatera] --> S1[Systemet tar emot uppgifter]
    S1 --> S2[Kontrollerar uppgifter]
    S2 -->|korrekta| S3[Krypterar]
    S3 --> S4[Lagrar säkert]
    S4 --> S5[Visar bekräftelse]

    S2 -->|felaktiga| A1[Felmeddelande]

    S2 -->|ingen rättslig grund| A2[Sparas inte + meddelande]

    S4 --> E1[Tekniskt fel]
    S3 --> E2[Krypteringsfel]
