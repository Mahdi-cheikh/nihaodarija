# NihaoDarija 你好 — China Pocket Translator

An offline-first Progressive Web App (PWA) to help you communicate in China across
**Chinese (汉字 + pinyin)**, **English**, and **Tunisian Darja**.

**Developer:** Mehdi Cheikh — Master's in Artificial Intelligence, Henan University of Technology.

---

## What it does

- **Phrasebook (works 100% offline):** 110+ ready phrases in 7 categories — Essentials,
  Campus & Study, Food & Restaurant (incl. halal / no-pork questions), Transport & Directions,
  Emergency & Health, Shopping & Money, Numbers & Time. Each phrase shows the Chinese
  characters, pinyin, English, and Darja, with a **🔊 speak button** (plus a 🐢 slow button)
  so you can play the Chinese out loud to the person in front of you.
- **Live Translate:** free-text translation between the three languages using the free
  MyMemory service whenever you have a connection. Runs fine behind any VPN.
- **Save favourites**, search, light/dark mode, and a developer section.
- **Installable**: add it to your phone's home screen and it opens like a real app,
  even with no signal.

## Why it's built for China specifically

Google Translate is blocked in mainland China, so the **core never depends on it**.
The phrasebook is fully baked into the app and cached on your device — no internet, no
problem. The optional live-translate tab uses a service that is reachable in China and
works the same whether or not a VPN is running.

---

## How to run / install

It's a static web app — no build step.

**Easiest (recommended): host it free**
1. Put all files in one folder (keep the names as-is).
2. Upload the folder to any static host — **Netlify Drop** (drag & drop), **Vercel**,
   **GitHub Pages**, or **Cloudflare Pages**. You'll get an `https://…` link.
3. Open that link on your phone → browser menu → **Add to Home Screen**.
   (A service worker needs HTTPS, which these hosts give you for free.)

**Test on your computer**
```bash
# from inside the folder:
python3 -m http.server 8080
# then open http://localhost:8080
```

## Add your photo

Drop a square photo named **`developer.jpg`** into the same folder.
It will appear automatically in the Developer tab. Until then, a "MC" avatar shows instead.

## Files
- `index.html` — the whole app (UI + phrasebook + logic)
- `manifest.webmanifest` — PWA settings
- `sw.js` — service worker (offline caching)
- `icon-192.png`, `icon-512.png`, `icon-512-maskable.png`, `apple-touch-icon.png` — app icons
- `developer.jpg` — *(you add this)* your photo

© 2026 Mehdi Cheikh · v1.0
