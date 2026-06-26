# 2d-matrix-visualizer
Vibe-coded website so I can visualize matrices

# 2D Matrix Visualizer

An interactive 2D linear transformation visualizer built with pure HTML, CSS, and vanilla JavaScript — no frameworks, no build tools, single file.

> Inspired by [3Blue1Brown](https://www.3blue1brown.com/)'s visual approach to linear algebra.

**[Live Demo →](https://rajsrule.github.io/2d-matrix-visualizer/) https://rajsrule.github.io/2d-matrix-visualizer/**

***

## Features

- **Transformed grid** — coordinate grid shears, stretches, and rotates in real time as you edit the matrix
- **Smooth animations** — lerp-based transitions (~18%/frame) for all matrix changes
- **Drag to transform** — grab the î or ĵ vector tips directly on the canvas
- **Basic & Slider modes** — enter values by hand or sweep with range sliders (−4 to 4)
- **Determinant parallelogram** — toggleable purple fill showing the signed area; flips red when det < 0, with the value labeled at the centroid
- **Custom vectors** — add up to 6 vectors; each shows a dashed ghost at the original position and a solid arrow at the transformed position
- **Step-by-step calculations** — live matrix multiplication breakdown for both basis vectors
- **Touch support** — drag on mobile works too

***

## Usage

No install needed. Just open `index.html` in any modern browser.

```bash
git clone https://github.com/rajsrule/2d-matrix-visualizer.git
cd 2d-matrix-visualizer
open index.html   # macOS
# or just double-click index.html in your file manager
```

***

## Matrix Convention

Column-major. The 2×2 matrix is stored as `{ a, b, c, d }` where:

```
M = | a  b |
    | c  d |
```

- **Column 1** `[a, c]` → where **î** (x-axis unit vector) lands
- **Column 2** `[b, d]` → where **ĵ** (y-axis unit vector) lands

Transformation of any vector `[x, y]`:

```
x' = a·x + b·y
y' = c·x + d·y
```

***

## Design

- Dark mode only (`#0a0a0b` background)
- Accent colors: **blue `#4aaee8`** for î, **orange `#e8844a`** for ĵ
- Fonts: [IBM Plex Sans](https://fonts.google.com/specimen/IBM+Plex+Sans) + [IBM Plex Math](https://fonts.google.com/specimen/IBM+Plex+Math)
- Floating cards use `backdrop-filter: blur` with no hard borders — the blur blends into the canvas

***

## License

MIT
