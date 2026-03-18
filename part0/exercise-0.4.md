```mermaid
sequenceDiagram
   participant browser
   participant server

   note right of browser:user'new text->hello

  browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    activate server
    server-->>browser: GET https://studies.cs.helsinki.fi/exampleapp/notes
    deactivate server

    note right of browser:redirect the data and fetch new data on https://studies.cs.helsinki.fi/exampleapp/notes
```
