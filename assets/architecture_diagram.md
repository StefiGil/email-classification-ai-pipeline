```mermaid
flowchart TB
    classDef trigger fill:#ff6d5a,stroke:#c0392b,color:#fff,stroke-width:2px
    classDef transform fill:#6c5ce7,stroke:#4834d4,color:#fff,stroke-width:2px
    classDef app fill:#00b894,stroke:#00a383,color:#fff,stroke-width:2px
    classDef code fill:#fdcb6e,stroke:#e17055,color:#2d3436,stroke-width:2px
    classDef output fill:#0984e3,stroke:#06528f,color:#fff,stroke-width:2px

    A["Get many messages<br/>gmail.message<br/><br/>Fetches unread emails<br/>(filtered by label)"]
    -->
    B["Edit Fields<br/>manual<br/><br/>Extracts customer_name, customer_email,<br/>subject, body and email_id"]
    -->
    C["HTTP Request<br/>POST generativelanguage...<br/><br/>Gemini classifies: category, priority<br/>and generates summary"]
    -->
    D["Code in JavaScript<br/><br/>Parses AI JSON, formats bullets<br/>and builds slack_message payload"]
    -->
    E["Send a message<br/>slack.postMessage<br/><br/>Sends structured notification<br/>with direct email link"]

    class A trigger
    class B transform
    class C app
    class D code
    class E output
