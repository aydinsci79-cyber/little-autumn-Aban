# Little Autumn — Personal Planner

A self-contained, mobile-first installable PWA inspired by the supplied autumn planner reference. It uses independent page views, IndexedDB persistence (with a localStorage fallback), and stores photo attachments as data URLs inside the local planner database.

## Run locally

A service worker requires HTTP(S), so do not open `index.html` directly as a `file://` URL. From this folder run:

```bash
python -m http.server 8000
```

Open `http://localhost:8000` in a browser.

## Install on Android

1. Upload this folder to any static HTTPS host (for example GitHub Pages, Netlify, or your own web host).
2. Open the HTTPS address in Chrome on Android.
3. Open Chrome's menu and choose **Install app** or **Add to Home screen**.
4. Launch Little Autumn from the home screen. The service worker caches the application shell for offline use after the first successful load.

## Data, privacy and backups

- No account, login, analytics, or remote database is used. Planner records and attached photos are kept in the browser's IndexedDB on this device.
- Use **Settings → Download complete JSON backup** regularly. The backup includes habits, history, notes, memories and photo data.
- Restore replaces the current local planner data after confirmation.
- CSV exports habit/date/completion rows. PNG exports a designed monthly summary. PDF actions open a print-ready designed document; select **Save as PDF** in the browser print dialog.
- The folder picker is used only when the browser supports the File System Access API (typically Chromium desktop; Android support varies). It asks for user permission and creates the named subfolders. On unsupported browsers, use normal downloads and select a destination folder in the Android download/save UI.

## Notes

The supplied image is used only for extracted decorative artwork (the autumn cat/window and lantern details); the calendar, cards, navigation, progress ring, text, and controls are real HTML/CSS components. The reference itself is included in `assets/reference.png` for comparison. Google Fonts are an optional enhancement; system fallback fonts remain available offline.
