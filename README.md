# Milky-Way

Milky-Way is a browser-based OpenRouter model browser and chat tester in the root `index.html`. It has **Models** and **Chat** tabs, lets you inspect available model IDs and context lengths, and sends chat requests directly from the browser to OpenRouter. It is not a server-side key vault.

## Open locally

No package installation is needed. Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>. Requests require network access and a usable OpenRouter key.

## Configure and use

On first load, a settings dialog asks for a non-empty API-key value. The page stores the entered value in browser `localStorage` under `openrouter_key`; if a value is already stored, it fetches models instead of opening the dialog. The default selected model is `meta-llama/llama-3.1-8b-instruct:free`.

The Models tab fetches `/api/v1/models`, shows free models where available, and falls back to the first 30 returned models if none match its free-model filter. Select a model card to set the chat model and switch to Chat; cards show the model ID and context length when the service provides one. In Chat, submit a trimmed, non-empty message with the send button or Enter. The request goes to `/api/v1/chat/completions` with the selected model and the conversation history held in page memory. Loading states and API/network errors appear in the interface, and sending is disabled while a request is in progress.

## Key handling and conversation limits

The key is stored in local storage and used by browser-side requests, so it is accessible to the browser environment and should not be treated as secret. Avoid entering a personal key on a shared device; clear the page’s stored browser data when appropriate. For a real application, put privileged credentials behind a server-side proxy rather than embedding or exposing them in a browser-delivered page. Check OpenRouter’s current terms and pricing before sending requests.

Conversation messages remain in memory only and are included in later requests. Switching models does not clear the conversation, and the source has no message-length limit or chat-history persistence. The page has no separate application server; failures can come from the network, key, or external service. The root `index.html` is the documented interface; no server-side configuration or deployment setup is included.