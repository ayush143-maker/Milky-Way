# Milky-Way

A browser-based OpenRouter tester. The root `index.html` provides a model selector, an API-key field, and a chat area for trying model requests. It runs client-side and is not a server-side key vault.

## Open locally

No package installation is needed. Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Customize the page

The visible page is in `index.html`. You can revise its wording and presentation there, but take care not to remove or rename the model selector, API-key field, or chat area if you still want to use the tester. This repository has no separate asset directory in its listed root files; if you add local assets, keep their paths relative to `index.html` correct.

## API key safety

Use only your own API key. Do not put it in source code, commit it, or expose it in screenshots. Check OpenRouter’s current settings and usage terms before sending requests; model usage may incur charges. Do not publish or share your key.

## Manual review checklist

This is a checklist of actions to perform, not a record of verified results.

- Open the root `index.html` in a browser, or use the local preview steps above. Locate the model selector, API-key field, and chat area.
- Try the visible controls without entering or exposing a real key. If you choose to send a request, use only your own key and first review current usage terms and possible charges. Never include the key in screenshots or commit it.
- Inspect the page at a narrow mobile-sized viewport and a wide desktop-sized viewport. Check that the selector, key field, chat area, and any visible controls fit and remain usable.
- If you add local assets, check that their relative paths resolve from `index.html`.