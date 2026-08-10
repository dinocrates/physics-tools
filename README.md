# Physics Tools

Interactive tools for a calculus-based intro physics course (Physics I/II), built to demo live in
class. Each tool is a single self-contained HTML file — no build step, no dependencies. Open it
directly in a browser, or serve the repo with GitHub Pages.

[`index.html`](index.html) at the repo root is a landing page listing every tool — that's the page
GitHub Pages should serve as the site root. Tools are numbered in the order they show up in the
course.

## Tools

| # | Tool | Unit | Description |
|---|------|------|-------------|
| 00 | [Powers of Ten](tools/00-scale-of-physics/index.html) | Course opener | A scale-of-the-universe journey from the Planck length to the observable universe. Drag a log-scale slider (or use arrow keys) through 29 illustrated stops — subatomic particles, atoms, a crystal lattice, everyday objects, planets, and galaxies — each with its size and a human-scale comparison. |
| 01 | [Dimensional Analysis Lab](tools/01-dimensional-analysis/index.html) | Measurement & Units | Enter a value and units, and watch the factor-label conversion chain build itself step by step, with matching units canceling live. Supports length, mass, time, and volume, including compound units (`mi/hr`, `g/cm^3`) and exponents. |
| 02 | [Fermi Estimation Lab](tools/02-fermi-estimation/index.html) | Measurement & Estimation | Five classic order-of-magnitude problems (donut shops in a city, the original Fermi piano-tuners question, golf balls in a school bus, blades of grass on a football field, lifetime heartbeats) with every assumption on a live slider — drag one and watch the estimate recompute. Plus a blank chain for building your own estimate from scratch. |

## Running locally

Each tool is a standalone `index.html` — just open the file in a browser. No server or install
required.

## Publishing to GitHub Pages

1. Push `main` to GitHub.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Branch: **main**, folder: **/ (root)** → **Save**.

GitHub will serve `index.html` (the landing page) at the repo's Pages URL, and each tool at
`/tools/<number>-<name>/`.
