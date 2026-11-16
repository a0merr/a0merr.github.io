# a0merr.github.io

Personal site for Andrew Merritt, served by GitHub Pages at
<https://a0merr.github.io>.

Plain HTML and CSS. No build step, no JavaScript, and nothing loaded from
another origin. A `Content-Security-Policy` meta tag in each page enforces
that, so adding a CDN font, analytics snippet or inline `style=""` attribute
will be **blocked by the browser** until the policy is updated to allow it.

| File | Purpose |
|---|---|
| `index.html` | The whole site. Edit content here. |
| `style.css` | All styling. Light/dark follows the visitor's OS setting. |
| `404.html` | Served by GitHub Pages for any unknown path. |
| `favicon.svg` | Tab icon. |
| `og.png` | 1200×630 preview image shown when the link is shared (LinkedIn, Slack…). |
| `og-card.html` | Source for `og.png`; the regenerate command is in its header comment. |
| `.nojekyll` | Tells Pages to serve files as-is instead of running Jekyll. |

## Preview locally

Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Resume

The Resume buttons link to the PDF in the profile repo
(`a0merr/a0merr/Andrew_Merritt_Resume.pdf`), so rebuilding the resume there
updates this site too. There is no copy to keep in sync here.
