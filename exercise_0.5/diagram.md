```mermaid
    sequenceDiagram
        participant browser
        participant server

        browser->>server: GET https://studies.helsinki.fi/exampleapp/spa
        activate server
        server->>browser: HTML Document
        deactivate server

        browser->>server: GET https://studies.helsinki.fi/exampleapp/main.css
        activate server
        server->>browser: CSS Document
        deactivate server

        browser->>server: GET https://studies.helsinki.fi/exampleapp/spa.js
        activate server
        server->>browser: JS Document
        deactivate server

        browser->>server: GET https://studies.helsinki.fi/exampleapp/data.json
        activate server
        server->>browser: JSON Data
        deactivate server

        browser->>server: POST https://studies.helsinki.fi/exampleapp/new_note_spa
        activate server
        server->>browser: 201 Created
        deactivate server
```