sequenceDiagram
title New note SPA

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
  
    server-->>browser: status code 201
    
Note over browser: browser executes the event handler that renders notes to display