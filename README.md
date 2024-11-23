# BaseTheme-DemoSite

A demonstration site showing how to use [BaseTheme](https://github.com/ChristopherA/BaseTheme) - a minimal Jekyll remote theme for GitHub Pages. This demo includes both simple web pages and blog posts.

## Features

### Core Features (Always Included)
- 🪶 Minimal, no-bloat foundation
- 🔍 SEO-friendly metadata
- 🗺️ Search engine sitemap
- 📱 Mobile-first responsive design
- ♿️ Accessibility built-in
- 🌙 Dark mode support
- 🖨️ Print-friendly styles
- 🚫 No JavaScript required
- 🎨 Easy to customize

### Optional Features (Remove If Not Needed)
- 📝 Automatic page layouts (reduces front matter boilerplate)
- 📖 Automatic page titles from headings
- 📑 Multiple page support with navigation
- ✍️ Blog post support
- 📰 RSS feed for blog posts

## See It In Action
- View the [live demo](https://christophera.github.io/BaseTheme-DemoSite/)
- See [BaseTheme](https://github.com/ChristopherA/BaseTheme) for core features
- Full template files in this repository

## Quick Start

1. Use GitHub's "Use this template" button to create your repository
2. Edit `_config.yml`:
    ```yaml
    # Theme Settings
    remote_theme: "ChristopherA/BaseTheme@main"
    
    # Core Plugins (from BaseTheme - do not remove these)
    plugins:
      - jekyll-remote-theme    # Required for remote themes
      - jekyll-seo-tag        # Required for SEO meta tags
      - jekyll-sitemap        # Required for search engines

    # Optional Plugins (remove these if you don't use them)
      - jekyll-default-layout     # Optional - removes need for layout in front matter
      - jekyll-titles-from-headings  # Optional - removes need for title in front matter
    
    # Blog Features (remove this section if not using blog posts)
      - jekyll-feed  # Optional - adds RSS feed for blog posts
    
    # Site Settings
    title: "Your Site Title"
    description: "Your site description"
    url: "https://yourusername.github.io"
    baseurl: "/your-repo-name"  # Leave empty if hosting at root URL
    
    # Navigation (remove pages you don't use)
    navigation:
      - title: Home
        url: /
      - title: About    # Remove if not using About page
        url: /about/
      - title: Blog     # Remove if not using blog
        url: /blog/

    # Blog Settings (remove if not using blog posts)
    feed:
      path: feed.xml
      posts_limit: 20
    ```
3. Enable GitHub Pages in your repository settings

## File Structure
```
.
├── _config.yml          # Site configuration
├── _pages/             # Static pages (optional)
│   └── about.md        # Example page (remove if not using)
├── _posts/             # Blog posts (remove if not using blog)
│   └── YYYY-MM-DD-*.md # Post files
└── index.md            # Home page
```

## Creating Content

### Static Pages (Optional)
Create pages in `_pages/` (remove directory if only using home page):
```yaml
---
layout: default
title: "About"
description: "About this site"  # Optional but good for SEO
permalink: /about/
---
Welcome to my site!
```

### Blog Posts (Optional)
If you want a blog, add posts in `_posts/` (remove directory if not using blog):
```yaml
---
layout: post
title: "My First Post"
description: "Introduction"  # Optional but good for SEO
date: 2024-11-21
---
Hello world!
```

## License

Released under [CC0](LICENSE) ("No Rights Reserved"). Use freely without attribution.

## Author

Created by Christopher Allen ([GitHub @ChristopherA](https://github.com/ChristopherA))
