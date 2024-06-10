```mermaid
sequenceDiagram
    actor user
    participant browser
    participant server
    participant database

    activate user
    user->>browser: saisir une note
    user->>browser: valider la note

    activate browser
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    

    activate server
    server->>database: new_note
    deactivate server

    activate database
    database-->>server: new_note
    deactivate database

   server-->>browser: note enregistrée
   deactivate browser

   deactivate user
```