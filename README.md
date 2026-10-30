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

## API key and data safety

This is a client-side page, not a secure place to store credentials. Any API key entered into a browser-delivered page is available in that browser environment and should not be treated as secret from the person using the browser. Do not hard-code a key in `index.html`, commit it, or include it in screenshots, copied logs, or shared troubleshooting details. The listed root files contain no `.env.example` or server-side configuration; do not add or assume environment variables as a substitute for a secure backend.

Use only your own API key. If a key is exposed, take appropriate steps to revoke or replace it. Check OpenRouter’s current settings and usage terms before sending requests; model usage may incur charges. Do not publish or share your key.

## Browser and platform reliability review checklist

This is a checklist for a future review, not a record of completed testing or verified results.

- Review the page in current desktop browsers relevant to your audience and on mobile browsers such as Safari on iOS and Chrome on Android where applicable. No compatibility results are recorded here.
- Use developer tools to inspect the console and network panel when loading the page and, if you choose to send a request, when submitting it. Distinguish page-loading errors from API response, authentication, or network errors; inspect status and failure details without copying or exposing the API key.
- Inspect `index.html` for local asset paths and external requests. Confirm any local files you add resolve from the page, and check external request failures rather than assuming the page has no dependencies because the listed root has no asset directory.
- Compare a narrow mobile-sized viewport with a wide desktop-sized viewport. Check that the model selector, API-key field, chat area, and visible controls fit and remain usable.
- If you test a live request, use only your own key, review current usage terms and possible charges first, and do not include the key in screenshots or shared logs.

## Manual review checklist

These are review steps, not verified results.

- Open the root `index.html` or use the local preview steps above. Locate the model selector, API-key field, and chat area.
- Review visible controls without entering a real key. If you choose to send a request, follow the API key safety guidance and inspect the result without exposing the key.
- After adding assets or changing layout, repeat the path, network, and viewport checks above.

## Accessibility review checklist

These are future review checks, not verified accessibility results.

- Use Tab and Shift+Tab to check keyboard access and logical focus order for the model selector, API-key field, chat area, and other visible controls. Check that focus is visible.
- Review the selector and key field for meaningful labels and other controls for names that communicate their purpose. Check whether request feedback and chat updates can be identified without relying only on visual changes.
- Check text, field-label, and control contrast against page backgrounds, including at narrow viewports.
- If you add images or motion effects, check text alternatives for informative images and behavior with the operating system's reduced-motion preference enabled.