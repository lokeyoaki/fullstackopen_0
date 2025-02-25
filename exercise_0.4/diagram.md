sequenceDiagram
    participant browser
    participant server

    browser->>server: GET https:studies.helsinki.fi/exampleapp/notes
    activate server
    server->>browser: HTML Document
    deactivate server