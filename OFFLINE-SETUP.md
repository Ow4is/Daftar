# Daftar offline preparation — action required

This package is **not ready to deploy** until you add the two third-party JavaScript files below. The environment used to prepare this package could not download them. No empty or fake library files were included.

Download these exact files using a browser and save them in the `libs/` folder:

1. `https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js` → `libs/html2canvas.min.js`
2. `https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js` → `libs/jspdf.umd.min.js`

Do not change their filenames. The Tajawal online font stylesheet has been removed; the browser uses fallback fonts. Original accounting application code and storage keys were not intentionally changed.

The updated service worker pre-caches all core assets including PDF libraries; installation fails if one is absent. The service worker is scoped to the hosting directory and handles only same-origin GET requests. Publish all files together on HTTPS, visit online once, then test from the iPhone Home Screen in airplane mode. Do not use real accounting records before verifying export, restore, offline PDF, and persistence.

This is a code-level preparation, not a verified iPhone runtime test. Keep the original ZIP as backup.
