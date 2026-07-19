<div align="center">

# 🛍️ Thaila

### The family grocery list that actually speaks your language.

**[▶ Open the app →](https://saj1919.github.io/thaila/)**

*Search in English, Marathi, or however you type it. Build a list. Tick off what
you already have. Share it on WhatsApp in one tap — and whoever you send it to
can edit it too.*

`No app to install` · `No sign-up` · `Nothing stored on any server` · `Free forever`

</div>

---

## The idea

Every household runs on the same tiny question: *"what do we need from the store?"*
— usually answered by a half-remembered list on WhatsApp, a photo of the fridge,
or three people buying the same packet of poha.

**Thaila** turns that into one shared, living checklist. Search the item, add it,
and mark it off once it's in the house. The list always shows two things at a
glance: **what you already have** and **what's still to buy**. Send it to family,
they tick and add their bit, and send it back — no accounts, no apps, just a link.

---

## What makes it nice

### 🔎 Search that understands how you actually type
Type it in English, in Marathi, in Devanagari, or in your own spelling — Thaila
figures it out with a built-in vocabulary of 300+ everyday terms **plus** phonetic
matching, so near-misses still land.

| You type… | You get |
|---|---|
| `doodh` · `दूध` · `milk` | 🥛 Milk |
| `mith` · `meeth` · `मीठ` | 🧂 Salt |
| `kanda` · `कांदा` | 🧅 Onion |
| `tup` · `toop` | 🫙 Ghee |
| `karle` | 🥒 Bitter gourd |
| `nachni` | 🌾 Ragi flour |
| `peeth` · `atta` | 🌾 Atta |
| `bhendi` · `shevga` | 🥬 Okra · Drumstick |

Spelled it three different ways? Doesn't matter — `mith`, `meeth`, and `meet` all
find salt.

### 🎙️ Voice search
Tap the mic and just say it. Great for when your hands are full in the kitchen.

### ✅ A checklist, not just a list
This is the heart of it. Every item has a tick. Mark things off as you buy them —
bought items dim, get a **"✓ Got"** badge, and sink to the bottom. A little progress
bar shows *"6 of 9 bought,"* and the bar at the bottom always tells you
**how much you still need to buy**. The list is a live picture of the pantry.

### 📲 One-tap WhatsApp sharing — and it's editable
Hit **Share on WhatsApp** and it sends a tidy message plus a link:

```
🛍️ Thaila list — 3 got / 5 to buy

Still need:
⬜ Onion — 1 kg ×1
⬜ Toor Dal — 1 kg ×1
⬜ Amul Milk — 1 L ×2

Already have:
✅ Amul Butter — 100 g ×2

✏️ Open & edit: https://saj1919.github.io/thaila/#l=…
```

Whoever opens the link sees the exact same list — ticks and all — can add or
remove items, and share **their** updated version back. The whole list rides
inside the link, so it stays between the two of you.

### 🏷️ Browse by category
A clean category rail on the left (with its own quick filter) lets you wander the
aisles — dairy, vegetables, staples, snacks, household — with product photos, pack
sizes, and prices.

### 🔒 Private by design
No login. No database. No analytics. Your list lives in your browser and inside
the links you choose to share. That's it.

---

## Try it in 20 seconds

1. **[Open the app](https://saj1919.github.io/thaila/)**
2. Search `doodh`, `kanda`, `atta`… and tap **Add**
3. Open **View list**, tick off what you already have at home
4. Tap **Share on WhatsApp** → send it to the family
5. They edit, re-share — you always know what's left to buy

---

## For the tinkerers

Thaila is a single static page plus one data file — no build step, no server.

- **`index.html`** — the entire app (search, voice, checklist, sharing).
- **`products.json`** — the grocery catalog it searches, a periodically refreshed
  snapshot of everyday products (staples, fresh produce, household &
  personal-care) with names, pack sizes, indicative prices, and images.

Run it locally:
```bash
cd site
python3 -m http.server        # then open http://localhost:8000
```
Deploy it free on GitHub Pages: push these files to a repo, then
**Settings → Pages → Deploy from a branch → `main` / `root`**. Live in a minute.
Adding new search words is a one-liner: the `ALIAS` dictionary at the top of
`index.html` is just `term → english` pairs.

---

## Good to know

Prices, availability, and product details are **indicative** and may be out of
date — always confirm with your store before relying on them. Thaila is an
independent personal tool and isn't affiliated with any retailer or brand.

## License

© 2026 — Released under **CC BY-NC-ND 4.0**. Free to use and share for personal,
non-commercial purposes, with attribution. See **[LICENSE.txt](LICENSE.txt)**.

<div align="center">

**Made with ❤️ for the weekly grocery run.**

</div>
