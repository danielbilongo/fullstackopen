```mermaid
sequenceDiagram
    actor user
    participant browser
    participant server


    user->>browser: https://studies.cs.helsinki.fi/exampleapp/spa
    activate browser
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    deactivate browser

    activate server
    server-->>browser: HTML+spa.js
    deactivate server
```