# Malmö Watch Clinic — website

A 5-page static site: `index.html` (Hem), `tjanster.html` (Tjänster),
`galleriet.html` (Galleriet), `hitta-hit.html` (Hitta hit), `kontakt.html`
(Kontakt). No build step — open any file in a browser, or upload the whole
folder to any static host (Netlify, Vercel, GitHub Pages, or the business's
existing web hosting).

## Before going live

- **Photos**: the gallery and about-section images are placeholder line-art
  (`assets/images/gallery-*.svg`, `about-movement.svg`), not real photos.
  Swap them for real photography of the workshop and repairs — this will do
  more for the site than anything else on this list.
- **Hero video**: `assets/video/hero.mp4` is a compressed version (1280×720,
  muted, ~1.9 MB) of the uploaded `Rolex_1.mp4` for fast loading. The footage
  shows a Rolex dial and crown logo — confirm the business has the rights to
  use it commercially (its own footage/licensed stock vs. someone else's
  branded content), or swap in workshop footage instead.
- **Email address**: no contact email was provided, so the contact form
  currently only confirms submission in the browser — it isn't wired to send
  anywhere yet. Connect it to an email service (e.g. Formspree, a mailto
  fallback, or a small backend) once you have an address to send to.
- **Real photos of reviews aside**, the Google rating (4.9★, 79 reviews),
  address (Amiralsgatan 42, 211 58 Malmö), phone (+46 73 535 15 48) and
  opening hours were pulled from the current Google Maps listing for "Watch
  Clinic" — double-check these are still accurate before publishing.
- **Instagram**: linked to `instagram.com/malmo_watch_clinic` as given in the
  brief — confirm this is the correct handle.

## Structure

```
index.html         Hem — video hero, about, services teaser, reviews
tjanster.html       Tjänster — full service list + quote panel
galleriet.html      Galleriet — image grid + Instagram callout
hitta-hit.html       Hitta hit — map embed, hours, directions
kontakt.html         Kontakt — contact form + direct details
css/styles.css       All styling (one shared stylesheet)
js/main.js            Nav, language switch (SV/EN), form handling
assets/video/hero.mp4       Compressed hero video
assets/images/               Poster frame + placeholder gallery art
```

## Language switching

Every page defaults to Swedish. The SV/EN toggle in the header and footer
swaps text via `data-sv` / `data-en` attributes (see `js/main.js`) and
remembers the choice across pages using `localStorage`. To edit copy, find
the matching `data-sv="…"` / `data-en="…"` pair on the element — the visible
text and the `data-*` attributes should stay in sync.
