title part0 Exercise 0.5: Requests on SPA Load

browser->server:HTTP POST https://studies.cs.helsinki.fi/exampleapp/spa
server-->browser: HTTP status code 304 returns HTML
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
server-->browser: main.css
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/spa.js
server-->browser: spa.js

note over browser:
browser starts executing js-code
that requests JSON data from server
end note

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
server-->browser: [{ date: "2020-12-31T15:39:35.287Z", content: "" }, ...]

note over browser:
browser executes the event handler
that renders notes to display
end note
