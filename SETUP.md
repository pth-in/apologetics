# Hugo Blog Setup Guide

## What Has Been Created

Your Hugo blog is now set up with:

1. **Hugo Configuration** (`config.toml`)
   - Configured for GitHub Pages
   - Clean, simple theme setup

2. **Content Structure**
   - Homepage content (`content/_index.md`)
   - First blog post about Pantera claims (`content/posts/christian-responses-pantera-claims.md`)

3. **Custom Theme** (`themes/simple-blog/`)
   - Clean, minimal design
   - Excellent readability
   - Responsive layout
   - Beautiful typography

4. **GitHub Pages Integration**
   - GitHub Actions workflow (`.github/workflows/gh-pages.yml`)
   - Automatic deployment on push to main branch

## Next Steps

### 1. Install Hugo (if not already installed)

**Windows (using Chocolatey):**
```powershell
choco install hugo-extended
```

**Or download from:** https://gohugo.io/installation/

### 2. Test Locally

```bash
hugo server
```

Then visit http://localhost:1313

### 3. Initialize Git Repository (if not already done)

```bash
git init
git add .
git commit -m "Initial commit: Hugo blog setup"
```

### 4. Connect to GitHub

```bash
git remote add origin git@github.com:pth-in/apologetics.git
git branch -M main
git push -u origin main
```

### 5. Enable GitHub Pages

1. Go to your repository on GitHub
2. Navigate to Settings → Pages
3. Under "Source", select "GitHub Actions"
4. The site will automatically build and deploy

## Adding New Posts

1. Create a new file in `content/posts/` (e.g., `my-new-post.md`)
2. Add front matter:

```yaml
---
title: "Your Post Title"
date: 2024-01-15
draft: false
tags: ["tag1", "tag2"]
categories: ["Category Name"]
description: "A brief description"
---
```

3. Write your content in Markdown
4. Commit and push:

```bash
git add content/posts/my-new-post.md
git commit -m "Add new post"
git push
```

## Customization

### Change Site Title/Description

Edit `config.toml`:
```toml
title = 'Your Title'
[params]
  description = "Your description"
```

### Modify Theme Colors

Edit `themes/simple-blog/layouts/_default/baseof.html` and change the CSS variables:
```css
:root {
    --primary-color: #2563eb;  /* Change this */
    --text-color: #1f2937;      /* And this */
    /* etc. */
}
```

### Add Menu Items

Edit `config.toml`:
```toml
[menu]
  [[menu.main]]
    identifier = "about"
    name = "About"
    url = "/about/"
    weight = 2
```

## File Structure

```
apologetics/
├── .github/
│   └── workflows/
│       └── gh-pages.yml      # GitHub Actions deployment
├── archetypes/
│   └── default.md            # Post template
├── content/
│   ├── _index.md             # Homepage
│   └── posts/
│       └── christian-responses-pantera-claims.md
├── themes/
│   └── simple-blog/          # Custom theme
├── static/                    # Static files (images, etc.)
├── config.toml               # Hugo configuration
├── .gitignore
└── README.md
```

## Troubleshooting

### Hugo not found
- Make sure Hugo is installed and in your PATH
- Try `hugo version` to verify

### Build errors
- Check that all required files are present
- Verify `config.toml` syntax is correct

### GitHub Pages not updating
- Check GitHub Actions tab for build errors
- Ensure workflow file is in `.github/workflows/`
- Verify repository settings allow GitHub Pages

## Support

For Hugo documentation: https://gohugo.io/documentation/

For GitHub Pages: https://docs.github.com/en/pages

