<img width="1074" height="471" alt="image" src="https://github.com/user-attachments/assets/c2cb01c6-b05b-4ec0-abf0-0286866e7976" />

sequenceDiagram
    participant browser
    participant server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    activate server
    server-->>browser: HTTP status code 200 OK HTML document
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    server-->>browser: HTTP status code 200 OK the css file
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    activate server
    server-->>browser: HTTP status code 200 OK the JavaScript file
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>browser: [{ "content": "test spa", "date": "2025-08-05T17:22:23.434Z" }, { "content": "new", "date": "2025-08-05T17:37:14.101Z" }, ... ]
    deactivate server
