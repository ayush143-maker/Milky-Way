# Milky-Way

A browser-based OpenRouter tester with a model selector, an API-key field, and a chat area for trying model requests. Visitors can choose a model, enter their own key, and use the chat area to try a request. This is a client-side tester, not a server-side key vault; the README does not establish a separate backend capability.

## Open locally

No package installation is needed. Open `index.html` in a modern browser. To serve the project folder over HTTP, run this command from the project folder:

    python -m http.server 8000

Then visit http://localhost:8000.

## API key safety

Use only your own API key. Do not put it in source code, commit it, or expose it in screenshots. Check OpenRouter's current settings and usage terms before sending requests; model usage may incur charges.