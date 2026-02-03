# TC Agent Extension (VS Code)

Frontend-only VS Code extension for **TC Agent** (Trusted Computing assistant). This repo contains the extension UI and client logic; the backend runs separately.

## Requirements

- Node.js 18+
- VS Code 1.85+
- A running TC Agent backend

## Setup

```bash
npm install
npm run compile
```

Open the folder in VS Code and press **F5** to launch the Extension Development Host.

## Configure Backend URL

In VS Code settings:

```json
{
  "tcAgent.backendUrl": "http://<BACKEND_HOST>:6101"
}
```

Example (your current backend):

```json
{
  "tcAgent.backendUrl": "http://43.137.51.37:6101"
}
```

## Notes

- This repo does **not** include the backend.
- API keys are configured on the backend, not in this extension.

