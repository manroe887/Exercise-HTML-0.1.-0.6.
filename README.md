# Exercise-HTML-0.1.-0.6.
Latihan Belajar Dasar HTML
**0.4. (New note diagram)**
Simple Diagram:

```mermaid
sequenceDiagram;
    Browser ->>+ Server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    Server -->>- Browser : HTML document
    Browser ->>+ Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    Server -->>- Browser: the CSS file
    Browser ->>+ Server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    Server -->>- Browser: the JavaScript file
    Note right of Browser: The browser starts executing the JavaScript code that fetches the JSON from the server
    Browser ->>+ Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    Server -->>- Browser: [{ "content": "HTML is easy", "date": "2023-1-1" }, ... ]
    Note right of Browser: The browser executes the callback function that renders the notes
```

**0.5. (Diagram situation where the user goes to the single-page app)**
Simple Diagram of Single-Page App:

```mermaid
sequenceDiagram;
    Browser ->>+ Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    Server -->>- Browser: 201 Created ({"message":"note created"})
```
