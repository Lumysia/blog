---
# --- Core Content ---
title: '{{ replace .File.ContentBaseName "-" " " | title }}'
description: "A brief page description for SEO and previews."
date: '{{ .Date }}'
lastmod: '{{ .Date }}'
draft: true

# --- Taxonomies ---
tags: []
categories: []

# --- Author ---
authors:
  - Lumysia

# --- Featured Image ---
image:
  src: "" # Path to the image (e.g., /images/posts/hello.jpg)
  alt: "" # Alt text for SEO and accessibility
  caption: "" # Optional caption below the image

# --- Page Behavior ---
build:
  render: true # Set to `never` to prevent this page from being built
  list: true # Set to `never` to hide from lists (homepage, archives, etc.)
  publishResources: true

# --- Page Features ---
features:
  toc: true
  comment: true
  share: true
  math: false

# --- Advanced Configuration ---
code:
  copy: true
  maxShownLines: 50
seo:
  # Override the default social media image (which uses `image.src`)
  images: [] # e.g., ["/images/posts/hello-social.jpg"]
assets:
  # Load page-specific CSS or JS files (relative to the `assets` directory)
  css: []
  js: []
---

## Title 1

## Title 2
