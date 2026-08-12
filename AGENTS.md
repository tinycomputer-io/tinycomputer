# AGENTS.md

## Cursor Cloud specific instructions

This repository is `tinycomputer.io`: a single static HTML landing page (`index.html`) with
static assets (`fonts/`, `marks/`, favicons, images). It is deployed on Vercel and has **no build
step, no package manager, and no dependencies** (there is no `package.json`).

### Running the site (development)

There is no framework dev server. Serve the static files with any static file server from the repo
root, for example:

- `python3 -m http.server 3000` (Python is preinstalled), then open `http://localhost:3000/`.

Because the site is a single `index.html` plus static assets, editing a file and refreshing the
browser is the full dev loop. Note that a plain static server does not emulate Vercel's `cleanUrls`
/ `trailingSlash` rewrites from `vercel.json`; this does not matter for the current single-page site
but would if additional routes are added.

### Lint / test / build

There are no lint, test, or build commands in this repo. Deployment is handled by Vercel on push to
`main` (see `README.md`).

### Notes

- Product rows on the landing page link to external sites (`leaguemate.fyi`, `flashies.cards`), so
  clicking them requires network access.
