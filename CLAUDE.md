# Mangesh & Pranita — Marathi wedding invitation

Single-file static site (`index.html`, no build step). Push to `main` = live on GitHub Pages:
https://vv8446931264-max.github.io/mangesh-pranita-vivah/

## Flow
Mahadwar opening (temple doors; tap -> bell + music, doors swing inward, Ganesh glows in the sanctum, camera pushes
into the light) -> hero (Paithani silk card with the names) -> antarpat reveal over the couple portrait (tap lowers the
cloth + akshata shower) -> events -> calendar -> couple -> venue -> countdown -> contact -> closing (maroon, akshata button).
Originally ported from the owner's template `vv8446931264-max/vishal-poonam-wedding`; the envelope was replaced by the doors.
Wedding facts (names, families, events 12-13 Dec 2026, venue, WhatsApp) were taken from
`vv8446931264-max/mangesh-pranita-wedding-v2` (its `const C` block) and must match it character for character.
Keep both languages: Marathi (Devanagari) first, English second. The couple's names are NOT written in Devanagari
(spelling unconfirmed) — ask the owner before adding them.

## Assets
- `img/doors-tall.webp` — 1184x1328 temple doors. Door leaves are cut by CSS from the same image: doorway = image pixels
  x 205-979, y 268-1171 (inside the garlands and samai lamps so nothing in front of the doors moves). Change these
  numbers only if the image changes.
- `img/ganesh.webp` — gold Ganesh on pure black; always use `mix-blend-mode: screen`.
- `img/paithani.webp` — 1080 square Paithani card (hero). `img/band.webp` — peacock-kalash strip cut from its border.
- `couple.webp` — painted couple portrait (1024x1536), shown behind the antarpat.
- `audio/main.mp3` — "Indian Flute" by Antti Luode, CC BY 3.0 (Wikimedia Commons). Keep the credit in the footer.
  Never commit copyrighted film songs. The temple bell is synthesised with WebAudio (no file).
- `preview.jpg` — WhatsApp/OG card, 1200x630, under 300 KB. Rename the file whenever it changes (WhatsApp caches).
  Render it from HTML with headless Chrome; PIL garbles Devanagari.
- `incoming/` — the owner uploads new images here from the phone (GitHub > Add file > Upload files). Optimise,
  move into place, then delete from `incoming/`.

## Rules
- Guest links: `?to=Name` personalises the doors scene and hero (textContent only).
- Test at 375px wide; most guests open from WhatsApp on a phone. Respect prefers-reduced-motion.
- og:url / og:image are absolute URLs on this repo name, so do not rename the repo.
- The owner works from a phone only and prefers delegating builds to Sonnet and simple checks to Haiku.
