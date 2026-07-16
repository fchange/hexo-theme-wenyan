# Motion And Layout

## Motion System

Wenyan uses motion to explain state changes, never to decorate reading.

| Tier | Duration | Use |
| --- | --- | --- |
| Fast | `160ms` | Icon, button, color, and pressed feedback |
| Normal | `280ms` | Cards, theme glyphs, TOC state, and mobile navigation |
| Page | `420ms` | A single opacity-only page-content entrance |
| Header | Configurable, default `500ms` | Upstream-compatible `48rem` to `72rem` article transition |

All spatial motion uses `cubic-bezier(.22, 1, .36, 1)`. Color changes use a standard ease. `prefers-reduced-motion` reduces every animation and transition to effectively zero.

Long-form content does not use per-paragraph reveals, parallax, scroll scrubbing, cursor effects, or continuous background motion. These effects interfere with reading position and are outside the upstream design language.

The page entrance must not transform `.site-main`: a transformed ancestor changes the containing block of the fixed article sidebar and causes the TOC to scroll with the document.

## Horizontal Axis

- Home, lists, archives, pages, article content, and footer share a `48rem` content axis.
- Article content and the `300px` TOC form one centered `72rem` grid, matching the upstream template.
- The TOC is hidden below `1280px`.
- At `1280px` and wider, the TOC occupies the right grid column with a `40px` gap.
- Mobile content uses the available viewport minus stable side padding.
- The `15px` desktop scrollbar means measured content coordinates may appear `7.5px` left of `window.innerWidth / 2`; they are centered within `document.documentElement.clientWidth`.

## Accent Color

Wenyan accepts one source color through the `accent` configuration. CSS derives strong, muted, soft, and selection variants with `color-mix()` against the active light or dark theme tokens. Accent color communicates navigation, links, focus, selection, taxonomy, current TOC state, external destinations, search matches, and successful copy actions; it does not color page backgrounds, body copy, headings, cards, or the footer surface.
