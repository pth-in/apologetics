# Apologetics Blog

A clean and simple Hugo-based blog for evidence-based Christian apologetics and scholarly responses.

## Features

- Clean, minimal design focused on readability
- Responsive layout for all devices
- Fast loading with optimized Hugo static site generation
- GitHub Pages integration for easy deployment

## Setup

### Prerequisites

- [Hugo](https://gohugo.io/installation/) (extended version recommended)

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/pth-in/apologetics.git
cd apologetics
```

2. Run Hugo server:
```bash
hugo server
```

3. Open http://localhost:1313 in your browser

## Adding New Posts

Create a new markdown file in `content/posts/` with the following front matter:

```yaml
---
title: "Your Post Title"
date: 2024-01-15
draft: false
tags: ["tag1", "tag2"]
categories: ["Category Name"]
description: "A brief description of your post"
---
```

## Deployment

This site is automatically deployed to GitHub Pages via GitHub Actions when you push to the `main` branch.

The site will be available at: https://pth-in.github.io/apologetics/

## Theme

This site uses a custom "simple-blog" theme designed for readability and clean presentation of scholarly content.

## License

Content is provided for educational purposes. Please cite sources appropriately.

