sequenceDiagram
    title New note

Note over browser: user enters new note and clicks "submit"

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
  
    server-->>browser: status code 302

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
  
    server-->>browser: HTML
   
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
   
    server-->>browser: main.css

Note over browser: browser starts executing JS code that request JSON data from server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
   
    server-->>browser: main.js

Note over browser: browser executes the event handler that renders notes to display
    
    server-->>browser: [{ "content: "Hello", date: "2023-07-05T18:39:39.570Z" }, ... ]