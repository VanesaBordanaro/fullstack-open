sequenceDiagram
title Single Page App

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
  
    server-->>browser: HTML
   
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
   
    server-->>browser: main.css

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
   
    server-->>browser: spa.js
    
Note over browser: browser starts executing JS code that request JSON data from server    

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    
    server-->>browser: [{ "content": "Hello", "date": "2023-07-05T18:39:39.570Z" }, ...]
    
Note over browser: browser executes the event handler that renders notes to display