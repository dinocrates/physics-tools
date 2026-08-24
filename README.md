# Physics Tools

Interactive tools for a calculus-based intro physics course (Physics I/II), built to demo live in
class. Each tool is a single self-contained HTML file — no build step, no dependencies. Open it
directly in a browser, or serve the repo with GitHub Pages.

[`index.html`](index.html) at the repo root is a landing page listing every tool — that's the page
GitHub Pages should serve as the site root. Tools are numbered in the order they show up in the
course.

Every page (landing page included) has a light/dark theme toggle in the top-right corner of the
header. It defaults to following the OS/browser's `prefers-color-scheme`; clicking cycles
auto → light → dark → auto, and the explicit choice is remembered (via `localStorage`, shared
across all the tools) until cycled back to auto.

## Tools

| # | Tool | Unit | Description |
|---|------|------|-------------|
| 00 | [Powers of Ten](tools/00-scale-of-physics/index.html) | Course opener | A scale-of-the-universe journey from the Planck length to the observable universe. Drag a log-scale slider (or use arrow keys) through 29 illustrated stops — subatomic particles, atoms, a crystal lattice, everyday objects, planets, and galaxies — each with its size and a human-scale comparison. |
| 01 | [Dimensional Analysis Lab](tools/01-dimensional-analysis/index.html) | Measurement & Units | Enter a value and units, and watch the factor-label conversion chain build itself step by step, with matching units canceling live. Supports length, mass, time, and volume, including compound units (`mi/hr`, `g/cm^3`) and exponents. |
| 02 | [Uncertainty & Error Analysis Lab](tools/02-uncertainty-analysis/index.html) | Measurement & Uncertainty | What error bars actually mean, one page, three tabs. Repeated Measurements: take (simulated) pendulum-timing trials and watch a dot-plot histogram build up, with a wide gray bar for the spread of individual readings (±s) next to a narrow gold bar for the uncertainty on the mean (±SEM) that shrinks as 1/√N. Comparing Results: drag two measurements with independent uncertainties and get a live agree/marginal/tension verdict from their combined-sigma separation. Propagating Uncertainty: pick +, −, ×, or ÷ and watch absolute uncertainties combine in quadrature for sums/differences, or relative (percent) uncertainties combine for products/quotients. |
| 03 | [Fermi Estimation Lab](tools/03-fermi-estimation/index.html) | Measurement & Estimation | A live Fermi estimate for how many donut shops Temecula, CA needs, built for classroom demos: pose the question against an 8-bit map of the city, optionally stash the actual count for later, then reveal the factor-chain breakdown on your own pacing. Every assumption is a slider; the map fills in with live pins (donut shops in gold, population sampled in cyan) as the estimate updates. |
| 04 | [Vector Components Lab](tools/04-vector-components/index.html) | Vectors | How a single vector resolves into components with sin and cos, in 2D and in 3D (tabbed). 2D: drag magnitude/angle and watch the shaded right triangle (hypotenuse \|V\|, angle θ, legs Vx/Vy) move with it, formula plugged in live. 3D: magnitude + elevation + azimuth sliders drive two shaded, angle-arced right triangles in a rotatable scene — V down to the ground (elevation φ) for a horizontal shadow ρ, then that shadow split into x and z (azimuth θ). An optional "Play build" animation walks the construction in from scratch. |
| 05 | [Vector Addition Lab](tools/05-vector-addition/index.html) | Vectors | How vector components add together to build a resultant — one page, three tabs. 2D: drag magnitude/angle and watch x/y components sum in a long-addition-style ledger, with B toggling (animated) between "from origin" and "tip-to-tail," plus an optional parallelogram overlay showing A+B = B+A. 3D: the same construction with x/y/z sliders in a fully rotatable scene. î ĵ k̂: pick any vector (A, B, or R) and watch it get walked out one unit vector at a time, with the algebraic notation spelled out live. |
| 06 | [Vector Products Lab](tools/06-vector-products/index.html) | Vectors | What dot and cross products actually mean, geometrically, in a fully rotatable 3D scene (drag to orbit, scroll to zoom, no libraries — hand-rolled projection on canvas). Dot mode draws the literal "shadow" one vector casts on the other, color-coded by sign, on a glowing sunlit rail with an "Overhead view" button and an "Animate angle" sweep. Cross mode draws the parallelogram A and B span and the perpendicular result vector, so you can rotate the scene and confirm it really is perpendicular to both. |
| 07 | [Vector Balancing Lab](tools/07-vector-balancing/index.html) | Vectors | The classic force-table lab, top-down: masses hang over pulleys around a ring, each pulling with a force equal to its weight (F = mg). Drag any pulley or hanging weight directly to change its angle, or use the sliders; add or remove up to four forces (0–500 g each), and the ring drifts off-center — colored green/gold/red by how far from equilibrium you are — toward whatever's left over after every pull is summed. A "Show equilibrant" toggle draws the exact vector (and hanging mass) that would cancel the net force. A Challenges mode adds 7 built-in balancing puzzles (1 given force up to 3 at once) with locked "given" forces, a Submit-answer check, and a Reveal-answer option. |
| 08 | [1-D Motion Lab](tools/08-1d-motion/index.html) | Kinematics | Two cars pass a fixed reference pipe and drive off down the track, each independently set to constant velocity, constant acceleration, or a speed-up → cruise → slow-down trip, with its own start time and start position — built for racing, pursuit, and offset-start problems. Position, velocity, and acceleration build up live in three synced, scrubbable/draggable graphs, with four togglable overlays (off by default, to keep the graphs from getting busy): shade the area under a(t) or v(t) to see the matching Δv or Δx bracketed on the graph above, or drop a tangent line on x(t) or v(t) to see the matching instantaneous value on the graph below. Auto-detects and lists where the two cars' paths cross. |

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
