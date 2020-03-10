# Camino <small>Beta</small>

A simple, Apple-inspired KISS theme for Jekyll.

![Example](repo/example.png)

Camino is a Jekyll theme I have created for my own personal website. Camino is a simple, KISS theme for Jekyll that mostly takes inspiration from Apple's interface designs and supports dark mode, as well as the `dark-mode-toggle` utility provided by the Chrome developers.

Camino includes, but is not limited to, the following features:

- Custom accent colors
- Dark mode functionality (and toggle)
- Special `document` and `post` layouts for blogs and articles
- Responsive behavior

## Usage

In your `_config.yml`, add the following line:

```yml
remote_theme: alicerunsonfedora/camino
```

## Example `_config.yml`

```yml
# Standard Jekyll Information. These fields are also used in the navbar on the
# top of the website, as well as OpenGraph information.
title: My Site
author: Marquis Kurt
description: Welcome to my GitHub Pages website

# This tells Jekyll to load Camino.
remote_theme: alicerunsonfedora/camino

# These are the plugins necessary to get the theme working.
plugins:
  - jekyll-octicons
  - jekyll-sitemap
  - jekyll-feed
  - kramdown

# This is the email address to use when clicking "Email me" in the footer of the
# website.
webmaster_email: contact@example.com

# This path will point to images used for the article/document format. Camino will
# look in this path for images with the file name of the shortcode listed on a document
# page. For example, 'wrt181-assignment1.png'
doc_img_url: "/images/cwp/"

# This path will point to images used for covers on posts. Camino will look in this path
# for image covers with the page's date. For example, '2020-02-17-cover.png'
cover_img_url: "/images/covers/"

# These settings configure the navbar profile picture.
nav_profile:
  # The image path to the profile.
  img_url: "images/profile.jpeg"

  # Whether to disable the drop shadow.
  flat: false

# This setting controls the accent color on the website. The accent color affects buttons, links,
# and other places of the theme. The 'light' and 'dark' entries control what color is displayed
# in light mode and dark mode, respectively. The standard and highlight entries control the idle
# and hover states.
accent:
  light:
    standard: "rgb(52, 199, 89)"
    highlight: "#5dd27a"
  dark:
    standard: "rgb(48, 209, 88)"
    highlight: "#59da79"

# This list controls the links visible in the navbar.
navigation:
  - name: "Home"
    link: "/index.html"
  - name: "Blog"
    link: "/blog.html"

# These Markdown settings are used to register the syntax highlighter.
markdown: kramdown
kramdown:
  input: GFM
  syntax_highlighter: rouge
  syntax_highlighter_opts:
    css_class: 'highlight'
```
## Using document formats

To create a document/article for Camino, add the following front matter to your web page or Markdown file:

```yml
---
title: Document Title
subtitle: A fancy subtitle
layout: document
class: History 207
shortcode: hist207-one
date: 2018-08-29
---
```

- `title`: The title of the document
- `subtitle` The subtitle of the document
- `layout`: The particular layout for the page. Should be set to `document`
- `class`: This field can be used to denote an academic class or the purpose of the document.
- `shortcode`: The shortcode used to denote the name of the image to use in conjunction with `doc_img_url`
- `date`: The document's publish date

## License

Camino is open-source software licensed under the Mozilla Public License v2.