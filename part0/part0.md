# 0.4

    Browser->Server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note
    note right of Server: Server send a 302 redirection to /exampleapp/notes
    Server->Browser: Redirection
    Browser->Server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/notes
    Server->Browser: HTML-code
    Browser->Server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
    Server->Browser: main.css
    Browser->Server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.js
    Server->Browser: main.js
    note left of Browser: Browser executes Javascript function that fetches JSON data
    Browser->Server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
    Server->Browser: [{"content":"note content","date":"2023-08-13T10:54:15.761Z"},...]
    note left of Browser: Browser executes the code inside the callback to display the notes

# 0.5

    Browser->Server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/spa
    Server->Browser: HTML-code
    Browser->Server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
    Server->Browser: main.css
    Browser->Server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    Server->Browser: spa.js
    note left of Browser: Browser executes Javascript function that fetches JSON data
    Browser->Server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
    Server->Browser: [{"content":"note content","date":"2023-08-13T10:54:15.761Z"},...]
    note left of Browser: Browser executes the code inside the callback to display the notes

# 0.6

    Browser->Server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    Server->Browser: 201 Created
    note left of Browser: Browser executes Javascript function that fetches JSON data and diplay the new note
