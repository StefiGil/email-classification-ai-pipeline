```mermaid
flowchart TB
    classDef trigger fill:#ff6d5a,stroke:#c0392b,color:#fff,stroke-width:2px
    classDef transform fill:#6c5ce7,stroke:#4834d4,color:#fff,stroke-width:2px
    classDef app fill:#00b894,stroke:#00a383,color:#fff,stroke-width:2px
    classDef code fill:#fdcb6e,stroke:#e17055,color:#2d3436,stroke-width:2px
    classDef output fill:#0984e3,stroke:#06528f,color:#fff,stroke-width:2px

    A["Get many messages<br/>gmail.message<br/><br/>Fetches product inquiries<br/>from the website (unread emails)"]
    -->
    B["Edit Fields<br/>manual<br/><br/>Extracts sender, subject, body<br/>and customer contact info"]
    -->
    C["HTTP Request<br/>POST generativelanguage...<br/><br/>Gemini classifies the inquiry:<br/>technical, resale, sales or other"]
    -->
    D["Code in JavaScript<br/><br/>Parses the classification and<br/>sets the target team"]
    -->
    E["Send a message<br/>post: message<br/><br/>Routes to the right team<br/>(technical, sales or resale)"]

    class A trigger
    class B transform
    class C app
    class D code
    class E output
