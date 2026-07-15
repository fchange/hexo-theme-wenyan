# Hexo Theme Wenyan

[🇨🇳 中文](/README.zh.md)

Wenyan is a minimal, typography-first Hexo theme for personal blogs.

It is designed for calm writing, focused reading, and lightweight customization.

**Live demo:** [fchange.github.io](https://fchange.github.io/)

It combines:

- a quiet paper-like reading surface
- compact post lists inspired by `guangzhengli/nextjs-blog-template`
- a narrow article layout with optional right-side table of contents
- improved code blocks with language labels and a copy button

## Install

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

Main theme options live in [`_config.yml`](/_config.yml).

You will usually want to adjust:

- `logo`
- `navigation`
- `navigation_items`
- `social`
- `social_items`
- `home`
- `labels`
- `footer_info`
- `footer`
- `motion`
- `valine`

`navigation_items` and `social_items` are optional ordered list forms. When set, they take precedence over `navigation` and `social`:

```yml
navigation_items:
  - label: Articles
    link: /
  - label: Archives
    link: /archives/
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

## Features

- clean home hero and article listing
- light and dark themes with a persistent theme switcher
- responsive desktop and mobile navigation with Lucide icons
- archive pages matching the same reading rhythm
- article pages with sticky table of contents on wide screens
- configurable footer and friends page
- optimized code blocks with copy button
- WenKai webfont integration
- optional Valine comments
- optional MathJax support

Like the upstream template, the home page only lists posts with `featured: true` in front matter:

```yml
---
title: Featured post
featured: true
---
```

## Notes

- Search is not bundled. Use a Hexo search generator such as `hexo-generator-search`.
- If you want LaTeX rendering, install a renderer that fits your Hexo stack and keep `latex: true`.
- `source/css/theme.css` is the single stylesheet source and requires no build step.
- The production integration at [fchange.github.io](https://fchange.github.io/) is the reference implementation for the current theme release.

## Credits

This theme is adapted from:

- [`gaoryrt/hexo-theme-pln`](https://github.com/gaoryrt/hexo-theme-pln)
- [`guangzhengli/nextjs-blog-template`](https://github.com/guangzhengli/nextjs-blog-template)
- [Lucide Icons](https://lucide.dev/) (navigation and utility icons, ISC License)

## License

MIT
