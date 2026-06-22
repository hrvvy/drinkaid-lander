# DrinkAid Gummies — Landing Page

A self-contained, long-form marketing landing page for **DrinkAid** anti-hangover gummies (Singapore).

## View it

Open **`index.html`** in any modern browser — the entire design (CSS + JS) is inline in that one file. Images load from the local `assets/` folder.

For the smoothest experience (and to avoid the odd `file://` restriction), serve it locally:

```bash
python -m http.server 8000
# then open http://localhost:8000
```

On Windows you can also run the bundled helper: `./serve.ps1`

> Fonts (Hanken Grotesk, Bricolage Grotesque, Playfair Display) and the spinning-gummy hero video load from a CDN, so keep an internet connection for the first view.

## Editing

- **`index.src.html`** — the editable source.
- **`index.html`** — the served copy. After editing the source, sync it: `cp index.src.html index.html`.

Both are self-contained: CSS lives in the `<style>` block, JS in the `<script>` block near the bottom.

## Stack

Vanilla HTML / CSS / JS. No build step, no dependencies.

## Notes for a Shopify build

The CTAs currently link to a `#pricing` anchor — wire them to a real product → variant → add-to-cart → checkout. Re-host `assets/` on Shopify and rewrite the paths. Scope the global CSS reset to a wrapper so it doesn't bleed into the theme.
