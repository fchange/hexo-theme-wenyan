# Hexo Theme Wenyan

[🇨🇳 中文](README.zh.md)

Wenyan is a minimal, typography-first Hexo theme for personal blogs.

It is designed for calm writing, focused reading, and lightweight customization.

**Live demo:** [fchange.github.io](https://fchange.github.io/)

![Wenyan accent presets: Cinnabar, Pine, and Indigo](docs/images/accent-presets.png)

## Why Wenyan

Wenyan keeps the page quiet and lets typography carry the experience. It combines a compact editorial index, a focused long-form article layout, restrained motion, and Hexo-native content features without introducing a frontend build step.

The visual hierarchy follows [`guangzhengli/nextjs-blog-template`](https://github.com/guangzhengli/nextjs-blog-template), while the theme contract remains familiar to Hexo users.

## Install

Wenyan works with Hexo 6 or newer and uses EJS templates, plain CSS, and vanilla JavaScript.

1. Clone this repo into your Hexo site:

```bash
git clone https://github.com/fchange/hexo-theme-wenyan.git themes/wenyan
```

2. Update your Hexo root `_config.yml`:

```yml
theme: wenyan
```

3. Merge the options you need from `themes/wenyan/_config.yml`.

## Quick Start

After installing the theme, run your Hexo site locally:

```bash
hexo clean
hexo server
```

Then open the local preview URL printed by Hexo, usually `http://localhost:4000`.

For article pages with a table of contents, enable `toc: true` in the post front matter:

```yml
---
title: My Post
date: 2026-01-01
toc: true
---
```

## Configuration

Main theme options live in [`_config.yml`](_config.yml).

You will usually want to adjust:

- `logo`
- `accent`
- `navigation`
- `navigation_items`
- `social`
- `social_items`
- `home`
- `labels`
- `footer_info`
- `footer`
- `sketch`
- `motion`
- `search`
- `stats`
- `valine`

`navigation_items` and `social_items` are optional ordered list forms. When set, they take precedence over `navigation` and `social`:

```yml
navigation_items:
  - label: Articles
    link: /
  - label: Archives
    link: /archives/
```

Choose one of the three editorial accent presets, or provide one quoted six-digit Hex color. Wenyan derives stronger, muted, soft, and selection shades automatically:

```yml
accent:
  preset: cinnabar # cinnabar | pine | indigo
  color: ""        # for example, "#c24132"; overrides preset
```

The accent is intentionally limited to navigation state, link underlines and hover, active TOC entries, tags, external-link marks, input focus, text selection, copied state, and search highlights.

Inline icons ship with a hand-drawn sketch style by default, rendered live by an SVG turbulence + displacement filter — no icon assets are modified, and the site-brand logo stays crisp. Tune the wobble or switch it off:

```yml
sketch:
  enable: true           # set false for crisp geometric icons
  base_frequency: 0.062  # noise density — higher = tighter wobble
  scale: 6               # displacement strength — higher = rougher line
  animate: false         # cycle the noise seed for a "boiling" motion
```

The article header mirrors the upstream transition from `48rem` to `72rem`:

```yml
motion:
  header_expand: true
  duration: 500
```

The footer can be disabled or configured with supporting text and links:

```yml
footer:
  enabled: true
  text: © Your Name
  description: Writing, design, and technology.
  links:
    GitHub: https://github.com/yourname
    RSS: /atom.xml
```

Search uses Google site search without generating a local index. Busuanzi counters are also optional; both integrations are disabled by default:

```yml
search:
  enabled: true

stats:
  busuanzi: true
  endpoint: https://busuanzi.ibruce.info/busuanzi
```

## Features

- **Editorial reading:** compact featured-post index, narrow long-form content, sticky desktop TOC, and semantic year-grouped archives
- **Personalization:** light/dark mode, three accent presets, one-color custom accents, ordered navigation, and configurable footer
- **Content model:** categories, tags, linked posts, per-post TOC and comments, friends pages, and localized metadata
- **Utilities:** responsive Lucide navigation, copyable code blocks, optional Google site search, Busuanzi counters, Valine, and MathJax
- **Simple maintenance:** one readable stylesheet and no theme build step

Like the upstream template, the home page only lists posts with `featured: true` in front matter:

```yml
---
title: Featured post
featured: true
---
```

Useful per-post fields include:

```yml
---
title: Linked post
featured: true
toc: true
comments: false
link: https://example.com/original-article
---
```

## Notes

- Search opens Google site-search results and does not require a Hexo search generator.
- If you want LaTeX rendering, install a renderer that fits your Hexo stack and keep `latex: true`.
- `source/css/theme.css` is the single stylesheet source and requires no build step.
- The production integration at [fchange.github.io](https://fchange.github.io/) is the reference implementation for the current theme release.
- Accent derivation uses CSS `color-mix()`. Current evergreen browsers are recommended.

## Credits

This theme is adapted from:

- [`gaoryrt/hexo-theme-pln`](https://github.com/gaoryrt/hexo-theme-pln)
- [`guangzhengli/nextjs-blog-template`](https://github.com/guangzhengli/nextjs-blog-template)
- [Lucide Icons](https://lucide.dev/) (navigation and utility icons, ISC License)

## License

MIT
