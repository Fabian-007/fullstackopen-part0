``` mermaid
sequenceDiagram
    participant browser
    participant server

browser ->> server: Get https://studies.cs.helsinki.fi/exampleapp/spa
activate server
server -->> browser: HTML document
deactivate server

browser ->> server: Get https://studies.cs.helsinki.fi/exampleapp/main.cs
activate server
server -->> browser: the css file 
deactivate server

browser ->> server: Get https://studies.cs.helsinki.fi/exampleapp/spa.js  
activate server
server -->> browser: the JavaScript file 
deactivate server

Note right of browser: The spa.js file runs in the browser and fetches note data via data.json.

browser ->> server: Get https://studies.cs.helsinki.fi/exampleapp/data.json
activate server
server -->> browser: JSON data 
deactivate server

Note right of browser: The page is rendered dynamically without reloading — that's the "single page" aspect.
```
