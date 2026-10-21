## LongSeek Workshop

Jekyll site for the LongSeek workshop series on long-horizon information seeking
(same structure as the agentic search tutorial site, agentic-search.github.io).

- Each edition has its own page, e.g. `wsdm2027.md` -> `/wsdm2027/`.
- Edition content lives in `_includes/summary-<edition>.html`, `_includes/cfp-<edition>.html`,
  `_includes/schedule-<edition>.html`, `_includes/organiser-<edition>.html`, `_includes/contact-<edition>.html`,
  and organisers in `_<edition>_organisers/`.
- The site root redirects to the latest edition, set by `latest_edition` in `_config.yml`.
- To add an edition (e.g. SIGIR 2027): copy the include files and the organiser folder with the new edition name,
  add the collection to `_config.yml`, add an `elsif` branch in `_layouts/home.html`, add `<edition>.md` with its permalink,
  add it to the Editions menu in `_includes/nav-bar.html`, and update `latest_edition` in `_config.yml`.
- Header photo: put a Hong Kong photo at `assets/img/hongkong.jpg` (the header falls back to dark grey without it).
- Organiser photos: replace `assets/img/placeholder.svg` in `_wsdm2027_organisers/*.md` with each organiser's photo.
- Local preview: `bundle install && bundle exec jekyll serve`.
