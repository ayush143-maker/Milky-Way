# Milky-Way

**Milky-Way** is a browser-based OpenRouter tester. Its interface brings model selection, an API-key field, and a chat area into one page, making it a lightweight place to experiment with model requests from the browser.

## Open locally

The repository is a standalone HTML page, so no package installation is needed. Open index.html in a modern browser. If you need an HTTP preview, run:

    python -m http.server 8000

Then visit http://localhost:8000.

## API key safety

Use only an API key that belongs to you. Never paste a key into source code, commit it to the repository, or share a screenshot that exposes it. Check the current OpenRouter settings and usage terms before sending requests; model usage may incur charges. This project is a client-side tester, so do not assume that it provides a secure server-side key vault.
