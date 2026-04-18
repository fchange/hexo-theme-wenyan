# Hexo Theme Wenyan

[🇬🇧 English](/README.md)

`Wenyan` 是一个偏排版、偏阅读体验的极简 Hexo 博客主题。

它融合了这些方向：

- 纸张感的浅色阅读界面
- 参考 `guangzhengli/nextjs-blog-template` 的紧凑文章列表
- 文章页窄栏正文和右侧目录
- 更完整的代码块展示，包括语言标识和复制按钮

## 安装

1. 把主题拉到你的 Hexo 项目里：

```bash
git clone https://github.com/fchange/hexo-theme-wenyan.git themes/wenyan
```

2. 修改 Hexo 根目录 `_config.yml`：

```yml
theme: wenyan
```

3. 按需合并 `themes/wenyan/_config.yml` 里的主题配置。

## 配置

主题主要配置都在 [`_config.yml`](/_config.yml)。

通常需要优先修改：

- `logo`
- `navigation`
- `social`
- `home`
- `labels`
- `footer_info`
- `valine`

## 特性

- 首页简介区和文章列表
- 与整体风格统一的归档页
- 宽屏下带粘性目录的文章页
- 带复制按钮的代码块
- WenKai 字体集成
- 可选 Valine 评论
- 可选 MathJax 支持

## 截图

![](/screenShots/ver1.0-index.jpg)
![](/screenShots/ver1.0-article.jpg)

## 说明

- 搜索功能默认不内置，可以搭配 `hexo-generator-search` 等插件使用。
- 如果需要 LaTeX，请按你的 Hexo 渲染链安装对应 renderer，并保留 `latex: true`。

## 致谢

这个主题基于以下项目继续演化：

- [`gaoryrt/hexo-theme-pln`](https://github.com/gaoryrt/hexo-theme-pln)
- [`guangzhengli/nextjs-blog-template`](https://github.com/guangzhengli/nextjs-blog-template)

## License

MIT
