# a0merr.github.io

Personal site for Andrew Merritt, served by GitHub Pages at
<https://a0merr.github.io>.

Plain HTML and CSS. No build step, no JavaScript, and nothing loaded from
another origin - the fonts are self-hosted too. A `Content-Security-Policy`
meta tag in each page enforces that, so adding a CDN font, analytics snippet
or inline `style=""` attribute will be **blocked by the browser** until the
policy is updated to allow it.

The one `<script>` tag in `index.html` is a JSON-LD block: structured data
for search engines, which browsers never execute.

The motion is CSS too. The reading-progress line in the header, the content
that fades up as it scrolls into view, the layered hero and the nav marker for
the section on screen are scroll-driven animations and scroll markers - see
"Scroll-driven polish" in `style.css`. Browsers without those features, and
visitors who ask for reduced motion, get the same page standing still.

The project cards carry real output, copied by hand, so they need updating
when the projects change:

- **siglint** - the demo run from that repo's README, verbatim.
- **autolab** - `python quickstart.py` run in a clone, trimmed where marked.
- **axiom-backtest** - the walk-forward chart plots the per-fold OOS Sharpe
  from `docs/CASE_STUDY.md`. The bar heights live in `style.css` (the policy
  blocks `style=""`), the values in `index.html`'s tooltips and table.

| File | Purpose |
|---|---|
| `index.html` | The whole site. Edit content here. |
| `style.css` | All styling. Light/dark follows the visitor's OS setting; a print stylesheet at the end covers paper and save-as-PDF. |
| `404.html` | Served by GitHub Pages for any unknown path. |
| `favicon.svg` | Tab icon. |
| `favicon.ico`, `apple-touch-icon.png` | The same icon for clients that can't use an SVG, and for the iOS home screen. Re-export both if `favicon.svg` changes. |
| `robots.txt`, `sitemap.xml` | Point search engines at the one page. |
| `fonts/` | Geist and Geist Mono (Latin subset, variable weight), from Fontsource 5.3.0. SIL Open Font License; license texts alongside. |
| `og.png` | 1200×630 preview image shown when the link is shared (LinkedIn, Slack…). |
| `og-card.html` | Source for `og.png`; the regenerate command is in its header comment. |
| `.nojekyll` | Tells Pages to serve files as-is instead of running Jekyll. |
| `.github/` | A link check (on every change and weekly) and Dependabot for the actions it pins. |

## Preview locally

Serve the folder (opening `index.html` directly works, but browsers refuse
to load the self-hosted fonts from `file://`, so it falls back to system fonts):

```sh
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Resume

The Resume buttons link to the PDF in the profile repo
(`a0merr/a0merr/Andrew_Merritt_Resume.pdf`), so rebuilding the resume there
updates this site too. There is no copy to keep in sync here.
