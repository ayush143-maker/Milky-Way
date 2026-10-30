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

## Deployment-readiness checklist

The repository inventory lists `README.md` and `index.html`, with no scripts or separate build-output directory. No deployment configuration or completed deployment is verified here. The following are recommendations to check before and after publishing:

- [ ] **Select the correct root/output directory.** For this project as listed, use the project folder containing the root `index.html` as the published root, unless your chosen publishing process requires a different setting. Confirm that the resulting page entry point is `index.html`; do not point to a directory that omits it.
- [ ] **Check asset paths.** No separate asset directory is listed. If you add images, stylesheets, or other local files, confirm that each reference in `index.html` uses the correct path relative to that file, and that filenames and capitalization match.
- [ ] **Review configuration and secrets.** This is a client-side page, not a secure place to store credentials. Do not hard-code an API key in `index.html` or any browser-delivered file, or commit or share one. The listed root files contain no `.env.example` or server-side configuration; do not assume environment variables provide a secure substitute for a backend.
- [ ] **Review the page before publishing.** Check the model selector, API-key field, chat area, layout, and any added resources. Do not enter a real key just to preview the page. If you choose to send a request, use only your own key and consider possible charges first.
- [ ] **Preview after publishing.** Once published, open the resulting page using the URL provided by your chosen publishing process. Check that the page loads, the intended controls are present and usable, and any added assets load. Inspect the browser console and network panel if something is missing. This preview is a recommended check, not a verified result.

## Troubleshooting

These are diagnostic checks, not reports of known problems.

1. Confirm you opened the root `index.html`, the tester’s entry page. Check that the model selector, API-key field, and chat area are present.
2. If a page resource you added is missing, check its path relative to `index.html` and confirm the local file exists.
3. Inspect the browser console and network panel. Distinguish errors loading the page or local resources from failures on a request you chose to send; authentication, service responses, and network problems need separate diagnosis.
4. A live OpenRouter request depends on network access and the API service. This is distinct from loading the local HTML page. Do not copy an API key into shared logs, screenshots, or troubleshooting notes.

## API key and data safety

Any API key entered into a browser-delivered page is available in that browser environment and should not be treated as secret from the person using the browser. Do not hard-code a key in `index.html`, commit it, or include it in screenshots, copied logs, or shared troubleshooting details. Use only your own API key. If a key is exposed, take appropriate steps to revoke or replace it. Check OpenRouter’s current settings and usage terms before sending requests; model usage may incur charges. Do not publish or share your key.

## Contributor handoff

Keep changes scoped to the intended page content, controls, or layout. Preserve `index.html` and existing references; if adding or moving local assets, update their paths and keep filenames consistent. In your handoff, briefly describe what changed and which files or references were affected. Manually review the result before publishing. These are review steps, not verified results.

- Review the visible controls without entering a real key. If you choose to send a request, use only your own key and consider possible charges first.
- Review the page at narrow and wide viewport sizes; check that the selector, key field, chat area, and controls remain usable.
- After adding assets or changing layout, check their paths and inspect the browser console and network panel.
- After publishing, open the resulting page and check it again in the browser.

## Accessibility review checklist

These are future review checks, not verified accessibility results.

- Use Tab and Shift+Tab to check keyboard access and logical focus order for the model selector, API-key field, chat area, and other visible controls. Check that focus is visible.
- Review the selector and key field for meaningful labels and other controls for names that communicate their purpose. Check whether request feedback and chat updates can be identified without relying only on visual changes.
- Check text, field-label, and control contrast against page backgrounds, including at narrow viewports.
- If you add images or motion effects, check text alternatives for informative images and behavior with the operating system’s reduced-motion preference enabled.