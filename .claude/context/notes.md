# Project Notes

Session summaries and durable context for the cardozaresearch.com academic site.

## Session — 2026-08-12

- Rebuilt the CV page ([_pages/cv.md](../../_pages/cv.md)) from the real CV PDF: Education, Experience (Grad Researcher, TA, Undergrad Research Coordinator, NASA Ames, FLOW Lab), Presentations, Mentoring, Affiliations, Service. Added a "Download as PDF" button.
- CV PDF is downloadable: copied from OneDrive to [files/adam-cardoza-cv.pdf](../../files/adam-cardoza-cv.pdf). (`files/` dir was previously empty.)
- Filled in real publications in `_publications/`: journal article (Efficient derivative computation, Wind Energy Science 2026) + 2 AIAA SciTech 2022 conference papers. Removed the template example. Conference papers dated `2022-01-01`/`2022-01-02` to force stable newest-first ordering since both are Jan 2022. Category `manuscripts` = Journal Articles, `conferences` = Conference Papers.
- Portfolio custom ordering: [_pages/portfolio.html](../../_pages/portfolio.html) now sorts by an `order` front-matter field (`{% assign ordered_portfolio = site.portfolio | sort: 'order' %}`) instead of alphabetical. Each project has `order:` (WATT=1, DSM=2, PIV=3, DLT=4). Gotcha: a project WITHOUT an `order` field sorts to the TOP (nil sorts first) — every new project needs the field.
- PIV media: the Projects list layout does NOT render `header.teaser` images (that's grid-mode only), but it DOES render `excerpt` through markdownify — so media embedded in the `excerpt` front matter shows on the main page. Used this route to avoid switching the whole list to grid layout.
- Replaced the 8.4 MB PIV GIF with a 731 KB H.264 MP4 (11× smaller) via ffmpeg (`-crf 23 -pix_fmt yuv420p -movflags +faststart`). Used `<video autoplay loop muted playsinline>` in both the excerpt and PIV page body — behaves like a GIF. `muted` required for autoplay; `playsinline` prevents iOS fullscreen.
- Deleted [images/imageset_10_dual.gif](../../images/imageset_10_dual.gif) (kept only the .mp4). Note: GIF still lives in git history — removing it there would need a history rewrite, not worth it for one blob.
- Gotcha/finding: GitHub Pages CDN serves stale cached HTML from different edge nodes (user saw pages "last updated" on 11th vs 12th in Firefox). Not cookies — it converges after propagation; hard refresh forces fresh copy. The "GIF not on main page" report was this caching lag, not a real bug (deployed HTML already had the img tag + asset served 200).
