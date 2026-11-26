# Aura Olfactive

A single-page site for **Aura No. 1**, an extrait de parfum in fluted crystal, and the **Arabic spray collection**.

- Scroll-driven film: 200 frames in `frames/` are scrubbed on a canvas as you scroll
- The Aura No. 1 flacon turns once as it scrolls into view (96 frames in `rot/`, still photo as fallback)
- Four chapters, anatomy of the flacon with a pressable actuator and mist, scent notes
- Arabic collection (six 50 ml sprays and a discovery set) with a working bag: quantities, line totals and order total
- Liquid-glass navigation, frosted panels, cursor-led hover on every box

No build step and no dependencies. Fonts (Newsreader, Inter, Amiri) load from Google Fonts.

## Run locally

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Structure

```
index.html      page, styles and scripts
favicon.svg     site icon
frames/         scroll film, f001.webp to f200.webp
col/            Arabic collection photos
rot/            turn of the flacon, r001.webp to r096.webp
aura-no1.webp   still photo of the flacon (fallback for the turn)
act-*.webp      actuator sprites for the anatomy section
```

Prices live in `index.html`: each product card has a `data-price` on its Add button and a visible price next to it. Keep both in sync.
