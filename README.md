# Thaila — grab & go 🛍️

**Live site → https://saj1919.github.io/thaila/**
Repo → https://github.com/saj1919/thaila

A grown-up-funky grocery checklist for the family. Search products (English,
transliterated Marathi, Marathi, or voice), build a list, tick off what you
already have, and share it on WhatsApp as an **editable link**. Runs entirely in
the browser — free on GitHub Pages, no backend, no database, no sign-ups. The
shared list is encoded into the link itself, so it stays private to whoever you
send it to.

> If the live link 404s, enable Pages once: repo **Settings → Pages → Source:
> Deploy from a branch → main / root → Save**, then wait ~1 minute.

## Files
```
index.html      the whole app (search + voice + checklist + WhatsApp share)
products.json   the catalog it searches
LICENSE.txt     license (CC BY-NC-ND 4.0)
```

## Features
- **Smart search** — 300+ Marathi/Hindi terms plus phonetic matching on every
  product, so `mith`/`meeth`→salt, `doodh`→milk, `कांदा`→onion, `karle`→bitter
  gourd, `nachni`→ragi flour all just work.
- **Voice search** — mic button; speak your item.
- **Checklist** — tick items as you buy them; bought items sink down and show a
  "✓ Got" state. The list shows what you still need vs already have.
- **Editable share link** — the list (with ticks) travels inside the URL.

## Update the data
From the project root (where the scraper lives):
```bash
python3 make_products_json.py     # rebuilds products.json from your latest scrape
```
Then commit & push (see below). The demo `products.json` is replaced by your full catalog.

## Publish / update on GitHub Pages
First time (repo already created at github.com/saj1919/thaila):
```bash
cd site
git init
git add .
git commit -m "thaila"
git branch -M main
git remote add origin https://github.com/saj1919/thaila.git
git push -u origin main
```
Then enable **Settings → Pages → main / root**. Live at:
```
https://saj1919.github.io/thaila/
```
Later updates are just:
```bash
git add . && git commit -m "update" && git push
```

## Weekly auto-refresh
Use `refresh.sh` (in the project root) + a weekly cron job — full steps in `DEPLOY.md`.

## How sharing works
Build a list → **Share on WhatsApp**. It sends your items (⬜ to buy / ✅ already
have) plus a link like `https://saj1919.github.io/thaila/#l=…`. Whoever opens it
gets the list pre-loaded, edits it, and shares their updated link back.

> Personal reference list for household use. See LICENSE.txt.
