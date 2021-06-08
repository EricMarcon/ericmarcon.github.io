---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "memoiR"
subtitle: "Templates to publish well-formatted documents both in HTML and PDF formats"
summary: ""
authors: ""
tags: []
categories: []
date: 2020-06-08
lastmod: 2020-06-08
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: "Smart"
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []

url_code: "https://github.com/EricMarcon/memoiR"
url_project: "https://ericmarcon.github.io/memoiR/"
---

*memoiR* is an R package that provides templates to publish well-formatted documents both in HTML and PDF formats. Documents can be produced locally or hosted on GitHub, where GitHub actions can update the published documents continuously.

Long documents are the main purpose of this package. Along with a GitBook version to be read online, their PDF version based on the LaTeX class memoir can be highly customized.

Functions are provided to make the publication of the documents on GitHub very easy, including their continuous integration.
