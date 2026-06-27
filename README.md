# Hexo Theme Wenyan

[🇨🇳 中文](/README.zh.md)

Wenyan is a minimal, typography-first Hexo theme for personal blogs.

It is designed for calm writing, focused reading, and lightweight customization.

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
- `social`
- `home`
- `labels`
- `footer_info`
- `valine`

## Features

- clean home hero and article listing
- archive pages matching the same reading rhythm
- article pages with sticky table of contents on wide screens
- optimized code blocks with copy button
- WenKai webfont integration
- optional Valine comments
- optional MathJax support

## Notes

- Search is not bundled. Use a Hexo search generator such as `hexo-generator-search`.
- If you want LaTeX rendering, install a renderer that fits your Hexo stack and keep `latex: true`.
- The theme focuses on readable posts and does not include a full asset pipeline; keep custom scripts and styles in your Hexo site when possible.

## Credits

This theme is adapted from:

- [`gaoryrt/hexo-theme-pln`](https://github.com/gaoryrt/hexo-theme-pln)
- [`guangzhengli/nextjs-blog-template`](https://github.com/guangzhengli/nextjs-blog-template)

## License

MIT
