# InDrive

Static dashboard apps for the inDrive strategic expansion report, deployed on GitHub Pages.

## Versions

| Version | Entry URL | Description |
|--------|-----------|-------------|
| **Version 1 (Original)** | `/` (`index.html`) | Contest-winning dashboard layout with tabs for Executive Summary, regional deep-dive, Q&amp;A, chatbot, and battle-card generator. |
| **Version 2 (Alternate)** | `/v2.html` | Alternate UI with scenario planner and default-data flow. |

Both versions use the **same** build-time Gemini API key: the GitHub Actions workflow replaces `__GEMINI_KEY_PLACEHOLDER__` in **both** HTML files from the repository secret `GEMINI_KEY`.

Locally, until you inject a key at build time, AI features show a notice that the key is not configured.

## Deployment

On push to `main`, [.github/workflows/deploy-pages.yml](.github/workflows/deploy-pages.yml) builds `dist/` with the injected key and publishes to GitHub Pages.

Ensure the `GEMINI_KEY` secret is set in the repo (or org) settings.

## Getting started (local)

Open `index.html` in a browser for Version 1. To preview Version 2, open `v2.html`. For full AI behavior locally, mirror the CI step or temporarily replace the placeholder string with your key (do not commit real keys).
