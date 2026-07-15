# Upstream Reference

Wenyan is a Hexo port of `guangzhengli/nextjs-blog-template` (Ladder Theme).

- Repository: https://github.com/guangzhengli/nextjs-blog-template
- Reference commit: `c7f6154aa0834c8e2725d1ecdef3f81925dd28a6`
- Commit date: 2025-08-05
- Reference rule: preserve the upstream visual hierarchy and responsive behavior; only adapt framework and Hexo data contracts.

## License Status

GitHub reports no detected license for the reference repository and the repository tree contains no license file at the fixed commit. Before publishing copied source or assets, obtain permission from the upstream author or confirm the applicable license. Until then, treat the upstream as a design and implementation reference rather than a redistributable dependency.

## Visual Baseline

- Home/list content width: `48rem`
- Article shell width: `72rem`
- Article content maximum: `56rem`
- Desktop table of contents: `18.75rem`, visible from `1280px`
- Home title: `2.25rem`, bold
- Post title: `2rem`, bold
- Body: `1.1rem / 2rem`
- Typeface: LXGW WenKai Lite with Chinese system fallbacks
- Palette: white, near-black, neutral gray
- Decoration: underlined links, restrained rounded controls, no page cards or shadows
- Motion: navigation width transition, mobile sheet, active TOC state, smooth back-to-top

## Intentional Hexo Adaptations

- Next.js routes map to Hexo layouts and partials.
- Content Collections fields map to Hexo front matter.
- `featured: true` selects posts shown on the first home page.
- Hexo's generated TOC replaces the React TOC parser.
- Vanilla JavaScript replaces Framer Motion, Radix Sheet, and React IntersectionObserver state.
- Valine and MathJax remain optional Hexo-specific integrations.
