# View Transitions Demo

E-commerce category → product detail page transition using the CSS View Transitions API (cross-document, MPA).

## Features

- **Cross-document view transitions** — product image morphs between listing and detail page
- **Zero JavaScript** — `@view-transition { navigation: auto }` + `view-transition-name` via CSS custom properties
- **`mix-blend-mode: multiply`** — removes white background from product images
- **Subgrid** — aligns product names across grid rows
- **Logical properties** throughout

## Browser Support

- Chrome 111+, Safari 18+ — full transitions
- Firefox — standard navigation, no transitions (yet)
- View Transitions are part of **Interop 2026**, full cross-browser support expected this year

## Progressive Enhancement

- No fallbacks needed — unsupported browsers simply navigate without animation
- No broken layout, no missing content, no JS dependencies

## Future: `attr()` Variant

The custom property approach (`style="--vtn: product-1"`) can be replaced with:

```css
view-transition-name: attr(id type(<custom-ident>), none);
```

- Derives `view-transition-name` directly from the element's `id` attribute
- Eliminates inline styles entirely
- Currently experimental (Chrome 133+), not fully reliable yet
- Tracked for revisit once `attr()` with `type()` stabilises

## Credits

- Product images borrowed from [Lentiamo.co.uk](https://www.lentiamo.co.uk)
- Built with guidance from the [CSS-First Agent Skill](https://skills.sh/luko248/css-first-skill/css-first) for Claude Code
