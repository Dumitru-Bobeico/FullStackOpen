<img width="1066" height="422" alt="image" src="https://github.com/user-attachments/assets/15813db3-bca7-4479-84bb-fd820d64f4bc" />

sequenceDiagram
    participant browser
    participant server

    Note right of browser: Payload {content: "hii", date: "2025-08-05T18:57:51.296Z"}
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: HTTP status code 201 Created
    deactivate server

    Note right of browser: No further HTTP requests, use the JavaScript fetched from the server to show the added note.
