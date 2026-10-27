# Shark Sea

An ASCII art aquarium of sharks and fish swimming around, live at **[shark.masstar.org](https://shark.masstar.org)**.

- Sharks cruise back and forth, and fish dart away when one gets close.
- Manta rays flap, sea turtles paddle, and jellyfish pulse as they drift, alongside swordfish, pufferfish, clownfish and more.
- Bubbles rise, seaweed sways, and the surface ripples.
- Click (or tap) anywhere to drop in a new fish.
- Respects `prefers-reduced-motion` by showing a still scene.

## Stream screens

Add text to the path and it shows up in the middle of the screen with a little bounce, which makes handy Starting Soon / BRB / ending screens (e.g. as an OBS browser source at 1920×1080):

| URL | Shows |
| --- | --- |
| `/starting-soon` | **Starting Soon** |
| `/brb` | **Be Right Back** |
| `/ending` | **Thanks for Watching** |
| `/brb/back-in-5-minutes` | **Be Right Back**, with "Back in 5 minutes" underneath |
| `/anything-you-like` | **Anything You Like** |

Dashes, underscores and `+` become spaces. All-lowercase text is capitalised automatically; include any capital letter (`/See-you-Tomorrow`) to keep your exact casing. Unknown paths go through `404.html`, which hands the path to the main page.

Everything lives in a single `index.html` with no build step or dependencies. Open it in a browser to run it locally.

## Adding creatures

Each creature is a `<script type="text/x-ascii">` block in `index.html`, drawn facing right. The page mirrors it automatically for fish swimming left, so new art just needs a new block with `data-kind="fish"` or `data-kind="shark"`. Optional extras:

- `data-speed`: speed multiplier (e.g. `0.5` for slow drifters).
- `data-color`: a fixed colour instead of a random one.
- `data-calm`: never darts away from sharks.
- Animation frames: separate them with a line containing only `%`; they play in turn every `data-flap` seconds (default `0.6`). Blank lines inside a frame are kept so frames can line up.

## Hosting

Served by GitHub Pages from the `main` branch. The `CNAME` file sets the custom domain, and DNS has a CNAME record pointing `shark` at `masstarvt.github.io`.

## License

[MIT](LICENSE) © 2026 MasstarVT
