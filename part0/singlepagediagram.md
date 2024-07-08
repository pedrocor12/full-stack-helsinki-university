```mermaid
sequenceDiagram
  participant browser
  participant server
  

  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
  activate server
  server-->>browser: HTML code 
  deactivate server

  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
  activate server
  server-->>browser: main.css
  deactivate server

  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
  activate server
  server-->>browser: spa.js
  deactivate server

  Note right of browser: Javascript code start to be executed
  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
  activate server
  server-->>browser: [{"content": "hola", "date":"2024-07-07"},...]

  Note right of browser: The callback function is executed by the broswer that renders the notes 

  
  
  

