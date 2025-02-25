```mermaid
    sequenceDiagram
        participant browser
        participant server

        browser->>server: GET https://studies.helsinki.fi/exampleapp/notes
        activate server
        server->>browser: HTML Document
        deactivate server

        browser->>server: GET https://studies.helsinki.fi/exampleapp/main.css
        activate server
        server->>browser: CSS Document
        deactivate server

        browser->>server: GET https://studies.helsinki.fi/exampleapp/main.js
        activate server
        server->>browser: JS Document
        deactivate server

        browser->>server: GET https://studies.helsinki.fi/exampleapp/data.json
        activate server
        server->>browser: JSON Data
        deactive server

        browser->>server: POST https://studies.helsinki.fi/exampleapp/new_note
        activate server
        server->>browser: Redirect to https://studies.helsinki.fi/exampleapp/notes
        deactivate server

        browser->>server: GET https://studies.helsinki.fi/exampleapp/notes
        activate server
        server->>browser: HTML Document
        deactivate server

        browser->>server: GET https://studies.helsinki.fi/exampleapp/main.css
        activate server
        server->>browser: CSS Document
        deactivate server

        browser->>server: GET https://studies.helsinki.fi/exampleapp/main.js
        activate server
        server->>browser: JS Document
        deactivate server
```