# Milky-Way

Milky-Way is a browser-based OpenRouter tester. The root `index.html` provides a model selector, an API-key field, and a chat area for trying model requests. The page runs client-side; it is not a server-side key vault.

## Open locally

No package installation is needed. Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Use and protect API keys

The page’s controls let you select a model, enter an API key, and use the chat area to try requests. A key entered into a browser-delivered page is available in that browser environment and must not be treated as secret from its user. Do not hard-code a key in `index.html`, commit it, or share it in screenshots, copied logs, or troubleshooting notes. Use only your own key; if it is exposed, take appropriate steps to revoke or replace it.

Requests depend on network access and the API service. Check OpenRouter’s current settings and usage terms before sending requests; model usage may incur charges. You do not need to enter a real key just to preview the page.

## Customize and troubleshoot

Edit visible wording and presentation in `index.html`. Preserve the model selector, API-key field, and chat area if you want to retain the tester interface. The listed root files include no separate asset directory; if adding local assets, keep their paths relative to `index.html` correct.

If the page does not load, confirm that you opened the root `index.html`. For a missing added resource, check its relative path and confirm the file exists. Distinguish failures loading the local page or its resources from errors returned by a request you chose to send; authentication, service responses, and network issues require separate investigation.

## Project files

- `index.html` — page entry point and tester interface.
- `README.md` — project documentation.

No package scripts, server-side configuration, or deployment setup are documented.