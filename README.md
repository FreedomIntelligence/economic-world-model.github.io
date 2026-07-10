# Economic World Models Initiative

Static GitHub Pages copy of `https://ecnomic-world-model.netlify.app/`.

## Files

- `index.html` contains the full page markup, styles, and the small "Read more" interaction.
- `1.png`, `2.jpg`, `3.jpg`, `4.jpeg`, `5.webp`, and `6.jpeg` are the page images copied from the Netlify site.
- `.nojekyll` tells GitHub Pages to serve the files directly without Jekyll processing.
- `.github/workflows/sync-peer.yml` mirrors pushes between the two intended GitHub Pages repositories.

## GitHub Pages targets

The requested `https://ewm.github.io/` address requires the account or organization name `ewm` and a repository named `ewm.github.io`. As of July 10, 2026, the GitHub account name `ewm` is already taken publicly, so the site has moved to the `economic-world-model` GitHub Pages namespace.

The intended GitHub Pages targets are:

- `economic-world-model/economic-world-model.github.io`, which publishes as `https://economic-world-model.github.io/`.
- `FreedomIntelligence/economic-world-model.github.io`, which publishes as `https://freedomintelligence.github.io/economic-world-model.github.io/`.

## Two-way sync setup

Create both repositories with `main` as the default branch and place this same repository content in both. Then add a repository secret named `EWM_SYNC_TOKEN` in both repositories. The token must have read/write Contents access to both repositories.

When a human push lands on either repository, the workflow force-mirrors that exact `main` commit to the peer repository. Pushes made by `github-actions[bot]` are skipped to prevent sync loops.
