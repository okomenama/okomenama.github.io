# okomenama.github.io

Amane Kubo's personal academic website, built with Jekyll and hosted on
GitHub Pages.

## Local development

```bash
bundle install
bundle exec jekyll serve
# open http://localhost:4000
```

## Adding a research entry

The [Research](/research/) page lists items from the `_research/` collection
— one Markdown file per topic.

1. Copy an existing file in `_research/` (e.g. `_research/climate-tipping-predictability.md`).
2. Update the front matter:
   - `title`, `date`, `venue`, `location`, `presentation_type` (Oral / Poster / Journal Article / …)
   - `tags`: pick from Climate Tipping, Climate Prediction, Earth System Model, Mathematical Statistics, Dynamical Systems, Quantum Computing, Data Assimilation, or add new ones
   - `pdf`: path to the slide PDF under `assets/pdfs/research/` (leave blank if none)
   - `paper_url`: DOI / paper link if published
   - `summary`: one or two sentences shown on the Research list and Home page
3. Drop the presentation PDF at the path referenced by `pdf`, e.g.
   `assets/pdfs/research/<slug>.pdf`.
4. Write the longer write-up as the Markdown body below the front matter.
5. Commit and push — the new entry appears automatically, sorted by `date`
   (newest first) on the Research page and (top 3) on the Home page.

## Updating the CV / Publications pages

Education, awards, funding, internships, activities, skills, publications,
and presentations are all driven by `_data/cv.yml`. Edit that file — the
[CV](/cv/) and [Publications](/publications/) pages regenerate automatically
on the next build. No HTML editing needed. Add new items under `publications`
or `presentations`; each list renders in the order it's written in the YAML
(put newest first), it is not auto-sorted by date.

To add/update the downloadable CV PDF (the button at the top of the CV page):

1. Export a CV PDF with any personal phone number removed (this is a public
   repo — anything under `assets/` is published as-is).
2. Place it at `assets/pdfs/cv/AmaneKubo_CV.pdf` (or update `cv_pdf` in
   `_config.yml` to point elsewhere).
3. Set `cv_pdf_available: true` in `_config.yml` so the download button
   appears on the CV page.

## Deployment

Pushing to `main` triggers GitHub Pages' built-in Jekyll build automatically
— no GitHub Actions workflow needed. Make sure the repository's
**Settings → Pages → Build and deployment → Source** is set to
"Deploy from a branch", branch `main`, folder `/ (root)`.

## Structure

```
_config.yml        site settings, nav, plugins
_data/cv.yml        structured CV data (education, awards, publications, …)
_research/           one file per research topic (collection)
_layouts/            default.html, research.html
_includes/            head, header, footer
assets/css/style.scss theme (light-blue palette, edit CSS variables at the top)
assets/pdfs/cv/       downloadable CV PDF
assets/pdfs/research/ presentation slide PDFs
assets/img/           profile photo (add profile.jpg and swap it into index.md)
index.md, research.md, publications.md, cv.md, contact.md
```
