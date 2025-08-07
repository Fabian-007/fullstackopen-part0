``` mermaid
sequenceDiagram
    participant browser
    participant server

   Note right of browser: User writes a new note and clicks 'save'
    browser ->> server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server -->> browser: [{content: "new note", date: "2025-08-07T16:34:55.947Z"}]
    deactivate server
  Note right of browser: The browser updates the UI without reloading the page
  ```
