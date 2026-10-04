# Knotebook PWA

This package converts the original `knotebook.html` into an installable Progressive Web App.

## Files
- `index.html` — your original Knotebook app with PWA metadata and service-worker registration.
- `manifest.webmanifest` — Android/Chrome install information.
- `sw.js` — app-shell/runtime caching.
- `icons/` — app icons.

## Install on Android using GitHub Pages
1. Create/open a GitHub repository.
2. Upload `index.html`, `manifest.webmanifest`, `sw.js`, and the `icons` folder.
3. In the repository, open Settings → Pages.
4. Set the source to the `main` branch and `/ (root)`, then save.
5. Open the generated Pages URL in Chrome.
6. Chrome menu (⋮) → Add to Home screen / Install app.
7. Confirm Install.

The Knotebook data continues to use browser storage as in the original app. The service worker does not replace that storage.

Note: PDF importing/rendering still uses PDF.js from cdnjs, as in the original file. The app shell itself is cacheable, but PDF.js may need one successful network load before it can be available from cache.
