# Fibonacci Spiral Generator

Generative art tool built with [p5.js](https://p5js.org), using phyllotaxis (golden angle) point distribution as the foundation for 13 distinct render modes.

**[Live demo →](https://lukaszlysakowski.github.io/fibonacci-spiral-generator)**

## What it does

Places 2000+ points in a sunflower/phyllotaxis spiral using the golden angle, then renders them through different visual systems — from topographic contour maps to space-filling curves to flow fields. Every mode reveals a different mathematical property of the underlying point distribution. All outputs export as plotter-ready SVG or PNG.

## Features

- **13 render modes** — Lines, Triangles, Dots, Voronoi Cells, Web/Network, Delaunay Triangulation, Traveling Salesman, Fibonacci Arms, Flow Field, Curved TSP, Hilbert Fill, Contour Lines, Hachures
- **Contour Lines** — groups points into radial bands drawn as smooth closed splines; looks like a topographic elevation map
- **Hachures** — outward radial tick marks tapering from center, evoking 18th century engraved cartography
- **Hilbert Fill** — sorts all points by Hilbert curve index and connects as a single smooth Catmull-Rom spline
- **Curved TSP** — nearest-neighbour tour rendered as a continuous Bézier path, bent by Perlin noise
- **Flow Field** — Perlin noise streamlines emitted from each phyllotaxis point
- **Fibonacci Arms** — connects every Nth point to reveal the counter-rotating spiral families in the distribution
- **SVG export** — plotter-ready vector output for every mode
- **PNG export** — full 1875×1875 resolution
- **Presets** — auto-named save/load system backed by localStorage

## Usage

Open `index.html` in a browser — no build step, no dependencies beyond the p5.js CDN.

Adjust controls and hit **Regenerate (Randomize)** for a random configuration, or tune each parameter manually. Export when you find something you like.

## Controls

| Control | What it does |
|---|---|
| Mode | Render algorithm — switches immediately |
| Count | Number of phyllotaxis points (100–10000) |
| Spacing | Radial spacing between turns |
| Size | Primary size parameter — line length, contour band count, hachure length |
| Line Weight | Stroke thickness |
| Wave Modulation | Distorts spiral point positions with a sine wave |
| Network Connections | Neighbour count for Network and Delaunay modes |
| Fib Arm Step | Which Fibonacci number to use for spiral arm connections |
| Flow Steps / Flow Scale | Trail length and noise feature size for Flow Field and Curved TSP |
| TSP Method | Spiral order or nearest-neighbour for TSP and Curved TSP |
| Background | Red, Black, White, Dark Blue |
| Regenerate | Randomises all parameters and re-renders |
| Save / Load Preset | Named presets stored in localStorage |
