# Shark Sea

An ASCII art aquarium of sharks and fish swimming around, live at **[shark.masstar.org](https://shark.masstar.org)**.

- Sharks cruise back and forth, and fish dart away when one gets close.
- Bubbles rise, seaweed sways, and the surface ripples.
- Click (or tap) anywhere to drop in a new fish.
- Respects `prefers-reduced-motion` by showing a still scene.

Everything lives in a single `index.html` with no build step or dependencies. Open it in a browser to run it locally.

## Adding creatures

Each creature is a `<script type="text/x-ascii">` block in `index.html`, drawn facing right. The page mirrors it automatically for fish swimming left, so new art just needs a new block with `data-kind="fish"` or `data-kind="shark"` (and an optional `data-speed` multiplier).

## Hosting

Served by GitHub Pages from the `main` branch. The `CNAME` file sets the custom domain, and DNS has a CNAME record pointing `shark` at `masstarvt.github.io`.

## License

[MIT](LICENSE) © 2026 MasstarVT
