# Aurora Mart — High-Fidelity Design

A high-fidelity UI build of the Aurora Mart mobile shopping app, converted as plain HTML/CSS from a figma design.
This is the polished, presentation-ready version developed from the
[low-fidelity wireframe](https://github.com/darun-2006/-Wireframing-Low-Fidelity-Design.git) of the same screen.

## What this is

Converted from a Figma high-fidelity design into a working HTML/CSS build — real color
palette, typography, imagery placeholders styled as content, and finished UI components — as
opposed to the grayscale, structure-only wireframe it was built from:

- **Purple/white brand palette** with gradient hero cards
- **Styled components** — rounded cards, pill buttons, colored status tags (e.g. "Save 38%",
  "Best Seller", "New", "Top Rated")
- **Realistic content** — product names, prices, ratings, and review snippets in place of
  greeked placeholder text
- **Icon set** — line-icon SVGs for nav, header actions, and category shortcuts
- **Polish details** — shadows, spacing rhythm, carousel dots, sticky bottom navigation

## Screens / sections included

All on one scrollable page:

1. Status bar + header (logo, cart, notifications, search icons)
2. Search bar with a usage tip
3. Category shortcuts (Beauty, Fashion, Electronics, Home & Kitchen, Grocery)
4. Hero banner / deals carousel
5. Flash Deals (4-item product grid with status tags)
6. Today's Savings (stat summary cards)
7. Recommended for You (personalized product grid)
8. Why Aurora Mart? (trust/feature list)
9. Top Customer Reviews
10. Quick Categories (list with entry points)
11. Shop the Look (community post cards)
12. Bottom navigation (Home, Cart, Deals, Orders, Account)

## Files

```
aurora-mart/
├── index.html   — page structure and content
├── styles.css   — full visual styling (colors, spacing, components)
├── assets/      — reserved for real product/lifestyle images
└── README.md    — this file
```

## How to run

No build step or dependencies. Just open `index.html` in any browser, or double-click the
file. For a live-reload dev view, you can also serve it locally:

```
cd aurora-mart
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Customizing

- All colors, radii, and spacing live as CSS variables at the top of `styles.css`
  (`--purple`, `--bg`, `--radius-lg`, etc.) — change a value there to restyle the whole page
  at once.
- Product and lifestyle photos are currently placeholder blocks with descriptive captions
  (e.g. "Modern product photo of Wireless Noise-Canceling Headphones..."). Drop real images
  into `assets/` and swap the placeholder `<div class="product-img">` blocks for `<img>` tags
  once you have real photography.
- The two-column product grid (`.product-grid`) is CSS Grid — adding another product card is
  just adding another `<article class="product-card">`.

## Using this in Figma / Adobe XD

  This project is plain HTML/CSS, not a native `.fig` or `.xd` file. To bring it into Figma or Adobe XD:
- **html.to.design plugin** (Figma) — import `index.html` directly as editable frames, layers, and text.
- **Manual trace** — open the page in a browser at 390px width (its base mobile size), screenshot each section, and paste into a Figma/XD frame, then trace over with native shape, text, and component tools.
- **Inspect for exact values** — use your browser's DevTools (right-click → Inspect) on any element to read its exact colors, spacing, and font sizes from `styles.css`, and match them 1:1 in your Figma styles/tokens.

## Relationship to the wireframe

This build follows the same section order, grid structure, and component grouping as the
[low-fidelity wireframe](https://github.com/darun-2006/-Wireframing-Low-Fidelity-Design.git). Only the visual layer changes between the
two versions — color, imagery, typography, and interaction polish are added here, while the
underlying information architecture stays identical.
