# Markdown to GitHub style web

> Because GitHub's `README` styling is actually really nice

## Background


[![](https://img.shields.io/badge/author-@jartigag-blue.svg?style=flat)](https://github.com/jartigag)
(forked from
[![](https://img.shields.io/badge/author-@KrauseFx-blue.svg?style=flat)](https://twitter.com/KrauseFx))

If you have a little side project, often you might want a simple landing page. The GitHub `README` rendering is really beautifully done: clean, simple and modern. The official [GitHub markdown to HTML API](https://developer.github.com/v3/markdown/) generates the HTML code, but not the stylesheets necessary to make it look nice.

## Solution

A simple script that converts a markdown (`.md`) file to a single HTML file, that includes all the HTML and CSS code inline, so you can host it anywhere.

There is no need to use this script if you already convert your markdown file to HTML, you can directly use the [stylesheet](https://github.com/KrauseFx/markdown-to-html-github-style/blob/master/style.css) of this repo.

## How it works

This project doesn't actually use the GitHub stylesheet, it's far too complex, and has legal implications.

Instead this project does 2 things:

- Convert the Markdown to HTML using [showdown](https://github.com/showdownjs/showdown), the most popular JS markdown parser. This could be replaced by the [official GitHub markdown to HTML API](https://github.com/KrauseFx/markdown-to-html-github-style/issues/2)
- Inject the GitHub-like CSS code at the bottom of the page

Resulting you get an HTML file that contains everything needed, so you can host the page on GitHub pages, AWS S3, Google Cloud Storage or anywhere else.

- Check out [the original markdown](https://github.com/KrauseFx/markdown-to-html-github-style/blob/master/README.md?raw=1) file of this `README`
- Check out the [raw generated HTML code](https://github.com/KrauseFx/markdown-to-html-github-style/blob/master/index.html) generated based on this markdown file on
- Check out the [GitHub rendered README](https://github.com/KrauseFx/markdown-to-html-github-style)
- Check out the [README rendered by this project](https://krausefx.github.io/markdown-to-html-github-style/)
