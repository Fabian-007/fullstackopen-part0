``` mermaid
sequenceDiagram
    participant browser
    participant server

browser ->> server: Get https://studies.cs.helsinki.fi/exampleapp/notes
activate server
server -->> browser: HTML document
deactivate server

browser ->> server: Get https://studies.cs.helsinki.fi/exampleapp/main.css
activate server
server -->> browser: the css file 
deactivate server

browser ->> server: Get https://studies.cs.helsinki.fi/exampleapp/main.js
activate server
server -->> browser: the JavaScript file 
deactivate server

Note right of browser: The browser initiates the javascript  code that fetches the JSON data from the server

browser ->> server: Get https://studies.cs.helsinki.fi/exampleapp/data.json
activate server
server -->> browser: JSON data 
deactivate server

Note right of browser: The executes the function that renders the fetched data 
```
 


