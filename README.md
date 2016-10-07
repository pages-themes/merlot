# `jekyll-theme-merlot`

Merlot is a Jekyll theme for [GitHub Pages](https://pages.github.com).

You can preview the theme at http://pages-themes.github.io/merlot.

### Usage

This theme was ported from the GitHub Automatic Page Generator to a Jekyll v3.3 theme gem.

To use it on a Pages site, add `theme: jekyll-theme-merlot` to your `_config.yml`.

```yml
theme: jekyll-theme-merlot
title: Custom title
description: Custom description.
show_downloads: true
google_analytics:
```

- To override the repository name or description from GitHub used in the header, set a `title` or `description`.
- Set `show_downloads` to `false` to hide the download buttons in the header.
- Set `google_analytics` to your tracking ID to enable pageview tracking.

This theme includes a single `default` layout. Markdown files should be prefixed with the following frontmatter.

```
---
layout: default
---

```

#### CSS

For CSS customization, create your own `/assets/css/core.css` in your project to replace the one from this theme, and override selected stylesheet properties.

```css
@import url("rouge-base16-solarized.css");
@import url("screen.css");
@import url("non-screen.css") handheld;
@import url("non-screen.css") only screen and (max-device-width:640px);
```

#### Syntax Highlighting

[Rouge](http://rouge.jneen.net/) is the default highlighter in Jekyll 3. This theme includes the `base16-solarized` stylesheet from Rouge.

To switch syntax highlighting colors to say `monokai`, install the `rouge` gem and run the following on the command line.

```
mkdir _scss
rougify style monokai > assets/css/rouge-monokai.css
```

Then replace `rouge-base16-solarized.css` with `rouge-monokai.css` in your version of  `/assets/css/core.css`

Other pygments highlighter themes should work as well.
