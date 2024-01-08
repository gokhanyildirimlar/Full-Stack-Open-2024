sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: JSON application
    deactivate server

    Note right of browser: The browser sends form data to the server on submit and gets back a JSON object to render on page without a need to reload the page 