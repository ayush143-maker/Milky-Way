# Milky-Way

A browser-based OpenRouter tester. The root `index.html` provides a model selector, an API-key field, and a chat area for trying model requests. This is a client-side tester, not a server-side key vault.

## Open locally

No package installation is needed. Open `index.html` in a browser. To serve the project folder over HTTP, run this from the project folder:

    python -m http.server 8000

Then visit http://localhost:8000. After editing, reload the page and review the interface in the browser.

## API key safety

Use only your own API key. Do not put it in source code, commit it, or expose it in screenshots. Check OpenRouter's current settings and usage terms before sending requests; model usage may incur charges.