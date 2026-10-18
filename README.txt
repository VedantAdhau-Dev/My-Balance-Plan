MY BALANCE PLAN — PWA / NETLIFY PACKAGE

FILES
- index.html: the app (HTML, CSS, JavaScript)
- manifest.webmanifest: installable app metadata
- service-worker.js: offline app-shell caching
- icons/: install icons in 192px and 512px sizes

DEPLOY TO NETLIFY
1. Extract this ZIP file.
2. Upload the extracted folder containing index.html, manifest.webmanifest,
   service-worker.js, and the icons folder to Netlify Drop:
   https://app.netlify.com/drop
3. Keep index.html and manifest.webmanifest at the root of the uploaded folder.
4. Open the deployed HTTPS URL on your phone.
5. In Chrome on Android, open the browser menu and choose "Install app" or
   "Add to Home screen" (the wording can vary).

PWA NOTES
- Installability and service-worker features require HTTPS in production.
  Netlify provides HTTPS for deployed sites.
- The service worker caches the app shell so the page can open offline after
  the first successful visit. First load and initial cache setup require internet.
- Checklist data remains in that browser's localStorage; it is not cloud-synced.
  Use the app's Backup and Restore controls to move data between devices.
- When you change the app files, increment CACHE_NAME in service-worker.js
  (for example, my-balance-plan-v2) before redeploying to ensure clients get
  the new cached version.
