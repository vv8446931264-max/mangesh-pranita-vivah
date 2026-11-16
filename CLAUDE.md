# Mangesh & Pranita — Marathi wedding invitation

Single-file static site (`index.html`, no build step). Push to `main` = live on GitHub Pages:
https://vv8446931264-max.github.io/mangesh-pranita-vivah/

## Origin
Ported from the owner's template repo `vv8446931264-max/vishal-poonam-wedding`
(tap-the-seal envelope opening -> hero -> quote -> events -> calendar -> couple -> venue -> countdown -> contact -> closing).
Wedding facts (names, families, events 12-13 Dec 2026, venue, WhatsApp) live in `index.html`; they were taken from
`vv8446931264-max/mangesh-pranita-wedding-v2`. Keep both languages: Marathi (Devanagari) first, English second.

## Assets
- `couple.webp` — painted couple portrait (1024x1536). Also the round cameo inside the envelope.
- `envelope-bg.jpg` — 1200x1200 square textile texture for the opening envelope (back, pocket, flap; CSS `cover`).
  Currently the template's saffron placeholder; to be replaced by a Paithani-style Marathi one.
- `audio/main.mp3` — "Indian Flute" by Antti Luode, CC BY 3.0 (Wikimedia Commons). Keep the credit in the footer.
  Never commit copyrighted film songs.
- `preview.jpg` — WhatsApp/OG card, 1200x630, under 300 KB. Rename the file whenever it changes (WhatsApp caches).
  Render it from HTML with headless Chrome; PIL garbles Devanagari.
- `incoming/` — the owner uploads new images here from the phone (GitHub > Add file > Upload files). Optimise,
  move into place, then delete from `incoming/`.

## Rules
- Guest links: `?to=Name` personalises the envelope and hero.
- Test at 375px wide; most guests open from WhatsApp on a phone.
- og:url / og:image are absolute URLs on this repo name, so do not rename the repo.
