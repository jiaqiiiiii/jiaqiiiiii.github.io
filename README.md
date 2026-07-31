# Personal site

A single-file personal academic page. No build step, no dependencies — just `index.html`.

## Putting it online

1. Create a repository on GitHub named **`YOUR-USERNAME.github.io`** (use your exact username; this is what makes it a user site rather than a project site).
2. Put `index.html` in the root of that repo and push.
3. Go to **Settings → Pages**, set *Source* to **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Wait a minute or two. The site will be at `https://YOUR-USERNAME.github.io`.

If you'd rather keep it as a project site (e.g. `github.com/YOUR-USERNAME/homepage`), the same steps work — the URL becomes `https://YOUR-USERNAME.github.io/homepage/`.

## Before you publish — things to fill in

Search the file for `TODO` and `YOUR-USERNAME`. The placeholders are:

- Email address, GitHub handle, ORCID (in the rail, and again in the Contact section)
- Exact titles for the CHR 2025 paper, the LDK 2025 poster, and the DH Benelux / OntoLex talks
- Links to PDFs and repositories for each publication
- Education entries in the CV timeline
- One line about your background in the About section

Drop your CV in the repo root as `cv.pdf` and the download button will work.

## The figure in the hero

The stacked bars are the one custom piece. Each row carries its own numbers:

```html
<div class="drift-row" data-v="58,34,8"><span class="drift-decade">1840s</span><div class="drift-track"></div></div>
```

The three values are percentages for the three senses and should sum to 100. Swap in real cluster distributions from your pipeline, update the legend labels underneath, and delete the "Illustrative figure" caption.

To use a different number of senses, add or remove values in `data-v` and add a matching colour rule in the CSS:

```css
.drift-seg[data-c="4"]{ background: #your-colour; }
```

## Adding entries later

Publications, talks, and service items are all `<li>` blocks inside `<ul class="entries">`. Copy one, change the text. The `<span class="tag">` element is the small outlined badge (`under review`, `best poster`) — omit it when you don't need it.

## Custom domain

If you want something like `jiaqizhu.nl`, add a file called `CNAME` containing just the domain, then point a CNAME record at `YOUR-USERNAME.github.io` in your DNS.
