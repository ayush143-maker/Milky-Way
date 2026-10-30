# Milky-Way

A browser-based OpenRouter tester. The root `index.html` provides a model selector, an API-key field, and a chat area for trying model requests. It runs client-side and is not a server-side key vault.

## Open locally

No package installation is needed. Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Customize the page

The visible page is in `index.html`. You can revise its wording and presentation there, but take care not to remove or rename the model selector, API-key field, or chat area if you still want to use the tester. The listed root files include no separate asset directory; if you add local assets, keep their paths relative to `index.html` correct.

## Troubleshooting

Use these as diagnostic checks; they do not indicate known problems.

1. Confirm you opened the root `index.html`, the tester’s entry page. Check that the model selector, API-key field, and chat area are present.
2. If a page resource you added is missing, check its path relative to `index.html` and confirm the local file exists.
3. Inspect the browser console and network panel. Separate errors loading the page or its local resources from failures on a request you chose to send; API authentication, service response, and network problems require different diagnosis.
4. A live OpenRouter request depends on network access and the API service. This is distinct from loading the local HTML page. Do not copy an API key into shared logs, screenshots, or troubleshooting notes.

## API key and data safety

This is a client-side page, not a secure place to store credentials. Any API key entered into a browser-delivered page is available in that browser environment and should not be treated as secret from the person using the browser. Do not hard-code a key in `index.html`, commit it, or include it in screenshots, copied logs, or shared troubleshooting details. The listed root files contain no `.env.example` or server-side configuration; do not add or assume environment variables as a substitute for a secure backend.

Use only your own API key. If a key is exposed, take appropriate steps to revoke or replace it. Check OpenRouter’s current settings and usage terms before sending requests; model usage may incur charges. Do not publish or share your key.

## Review checklist

These are review steps, not verified test results.

- Review the visible controls without entering a real key. If you choose to send a request, use only your own key and consider possible charges first.
- Review the page at narrow and wide viewport sizes; check that the selector, key field, chat area, and controls remain usable.
- After adding assets or changing layout, repeat the path and browser-console checks above.

## Accessibility review checklist

These are future review checks, not verified accessibility results.

- Use Tab and Shift+Tab to check keyboard access and logical focus order for the model selector, API-key field, chat area, and other visible controls. Check that focus is visible.
- Review the selector and key field for meaningful labels and other controls for names that communicate their purpose. Check whether request feedback and chat updates can be identified without relying only on visual changes.
- Check text, field-label, and control contrast against page backgrounds, including at narrow viewports.
- If you add images or motion effects, check text alternatives for informative images and behavior with the operating system’s reduced-motion preference enabled.