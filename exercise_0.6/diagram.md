```mermaid
    sequenceDiagram        
        browser->>server: POST https://studies.helsinki.fi/exampleapp/new_note_spa
        activate server
        server->>browser: 201 Created
        deactivate server
```