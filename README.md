# cardozaresearch.com

Personal academic website of Adam Cardoza — built with
[Jekyll](https://jekyllrb.com/) on the
[academicpages](https://github.com/academicpages/academicpages.github.io)
template (a fork of Minimal Mistakes), hosted on GitHub Pages at
**https://cardozaresearch.com**.

## Local development

Ruby is pinned to the version in [`.ruby-version`](.ruby-version) via `rbenv`.

```bash
# one-time
rbenv install        # installs the version in .ruby-version
gem install bundler
bundle install

# run the live-reload dev server
bundle exec jekyll serve --livereload
# → open http://localhost:4000
```

Edits to content/layouts hot-reload. **`_config.yml` changes require a server
restart.**

## Where things live

| What | Where |
|------|-------|
| Landing page (splash, no sidebar) | [`_pages/about.md`](_pages/about.md) |
| Research narrative | [`_pages/research.md`](_pages/research.md) |
| CV | [`_pages/cv.md`](_pages/cv.md) |
| Site config (name, links, SEO) | [`_config.yml`](_config.yml) |
| Header navigation | [`_data/navigation.yml`](_data/navigation.yml) |
| Publications (one file per paper) | [`_publications/`](_publications/) |
| Projects (one file per project) | [`_portfolio/`](_portfolio/) |
| Teaching & resources | [`_teaching/`](_teaching/) |
| PDFs, downloads (CV pdf, papers) | [`files/`](files/) |
| Images (hero, headshot, figures) | [`images/`](images/) |

Each collection directory has an `example-*.md` template file — copy it, rename,
fill it in, and delete the example once you have real content.

## Adding content

- **A publication:** copy `_publications/2025-01-01-example-publication.md`,
  rename to `YYYY-MM-DD-slug.md`, edit the front matter. A `.bib` export can be
  bulk-converted using the notebooks in [`markdown_generator/`](markdown_generator/).
- **A project:** copy `_portfolio/example-project.md`.
- **A resource / course:** copy `_teaching/example-resource.md`.

## Things still marked TODO

Search the repo for `TODO` — placeholders to fill in: Google Scholar / ORCID /
LinkedIn links in `_config.yml`, the hero image, your headshot (`images/profile.svg`),
and the research/CV prose.

## Deployment

Pushing to `master` triggers [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml),
which builds the site and deploys it to GitHub Pages at
**https://cardozaresearch.com**.
