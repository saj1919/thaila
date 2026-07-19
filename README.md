# Thaila — grab & go

A grown-up-funky grocery-list web app for your family. Search products (in
English, transliterated Marathi, or Marathi — plus voice search), build a list,
and share it on WhatsApp as an **editable link**. Whoever opens it can tweak the
list and re-share their version. Runs entirely in the browser, so it hosts free
on GitHub Pages — no backend, no database, no sign-ups. The shared list is
encoded into the link itself, so it stays private to whoever you send it to.

## Files
```
site/
├── index.html       the whole app (search + voice + list + WhatsApp share)
└── products.json    the catalog it searches
```

## Features
- **Multilingual search** — type `milk`, `kanda`, `दूध`, `tup`, `atta`, `batata`… it
  understands Marathi/Hindi terms and Devanagari and maps them to the right products.
- **Voice search** — mic button, toggle EN / मराठी.
- **Unavailable items included** — out-of-stock products are shown and tagged; a
  "Hide unavailable" toggle filters them out when you want.
- **Editable share link** — the list travels inside the URL; nothing is stored on a server.

## Put your catalog in
Generate `products.json` from your collected catalog CSV:
```bash
python3 make_products_json.py           # auto-finds the catalog CSV in data/
```
(The repo ships with a tiny demo `products.json` so the page works right away.)

## Preview locally
`fetch()` needs a server (not file://):
```bash
cd site
python3 -m http.server        # open http://localhost:8000
```

## Host on GitHub Pages (free)
1. Put the **contents of this `site/` folder** at a repo's root (so `index.html` and
   `products.json` are top-level):
   ```bash
   cd site
   git init && git add . && git commit -m "thaila"
   git branch -M main
   git remote add origin https://github.com/<you>/thaila.git
   git push -u origin main
   ```
2. GitHub → **Settings → Pages → Source: Deploy from a branch → main / root** → Save.
3. Live in ~a minute at `https://<you>.github.io/thaila/`.

## How sharing works
Build a list → **Share on WhatsApp**. It sends your items plus a link like
`…/thaila/#l=<encoded-list>`. Whoever opens it gets the list pre-loaded, edits it,
and shares their updated link back. All client-side.

> This is a personal reference list for your own household use.
