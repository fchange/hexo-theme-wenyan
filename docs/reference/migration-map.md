# Migration Map

| Upstream | Wenyan | Contract |
| --- | --- | --- |
| `src/app/layout.tsx` | `layout/layout.ejs` | Header wraps all generated pages |
| `src/components/header` | `layout/_partial/navigator.ejs` | Desktop nav, mobile sheet, social links |
| `src/app/page.tsx` | `layout/index.ejs` | Intro plus featured posts |
| `src/app/blog/page.tsx` | Hexo archive/list pages | Chronological post list |
| `src/app/blog/[...slug]/page.tsx` | `layout/post.ejs` | Article and wide-screen TOC |
| Post presentation | `layout/_partial/post/title.ejs`, `meta.ejs`, `comment.ejs` | Shared title, taxonomy, linked-post, statistics, and comment contracts |
| `src/components/mdx-components.tsx` | `.post-content` in `source/css/theme.css` | Markdown typography |
| `src/components/toc.tsx` | Hexo `toc()` plus `source/js/theme.js` | Nested TOC and active heading |
| `src/components/go-to-top.tsx` | `.back-top-link` | Back-to-top control |
| Site search command | `layout/_partial/search.ejs` plus `source/js/theme.js` | Optional Google site-search dialog without a generated index |
| Tailwind utility classes | `source/css/theme.css` | Single readable CSS source |
| Content Collections front matter | Hexo front matter | `title`, `date`, `featured`, excerpt/summary |

## Source Of Truth

`source/css/theme.css` is the only theme stylesheet. The legacy SCSS files and generated `m.min.css` were removed after the new stylesheet passed a real Hexo build.

## Fidelity Rules

1. Prefer upstream measurements over local historical styles.
2. Do not introduce paper textures, decorative gradients, ornamental Chinese motifs, or card-heavy layouts.
3. Preserve upstream responsive breakpoints: mobile navigation below `768px`, article TOC from `1280px`.
4. Hexo-only features must adopt the upstream monochrome typography and spacing.
5. Validate changes against the fixed upstream commit, not the upstream default branch.
