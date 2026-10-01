# kazybekkh.github.io

Plain HTML and CSS. No framework, no build step. GitHub Pages serves the
`main` branch root as-is (`.nojekyll` turns off Jekyll).

This is separate from kazybekkh.me. There is no CNAME on purpose.

## preview locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## add a post

1. Copy `writing/_template.html` to `writing/your-slug.html`.
2. Replace every `POST_` value (title, summary, slug, date) and the
   `datetime` attribute. Delete the `noindex` line.
3. Add one line at the **top** of the list in `writing/index.html`:
   `<li><a href="/writing/your-slug.html">title</a> <span class="date">2026-10-01</span></li>`
4. Add the same line at the top of the writing list in `index.html`.

**First post only:** in `index.html`, remove `hidden` from the writing
`<section>`. In `writing/index.html`, delete the `noindex` line.

## update "now"

Edit the one paragraph under `<!-- NOW -->` in `index.html`.

## add a build

In `index.html`, under `<!-- BUILDS -->`, copy an existing `<li>` and edit it.
Keep robotics first and keep the list to 4 or 5. Remove one if you add one.

To add a code link, replace that build's `<!-- TODO ... -->` comment with:

```html
<span class="links"><a href="https://github.com/Kazybekkh/REPO">code</a></span>
```

## house rules

- lowercase copy, no em dashes.
- links are the only blue thing.

## deploy

Push to `main`. Pages updates in about a minute.
