# BaseTheme-DemoSite

This is a demonstration and template site built using [BaseTheme](https://github.com/ChristopherA/BaseTheme). While BaseTheme provides a lean foundation for static sites on GitHub Pages, this DemoSite shows how to build upon that foundation, illustrating both basic usage for web pages and optional features such as blog posts.

Think of BaseTheme as your starting point - a foundational building block. This DemoSite shows you how to add additional blocks together for a complete lean website.

## Features

### Core Features (From BaseTheme)
- 🪶 Minimal, no-bloat foundation
- 📝 Automatic front matter generation
  - Page titles from first heading
  - Layouts based on content location
- 🔍 SEO-friendly metadata
- 🗺️ Search engine sitemap
- 📱 Mobile-first responsive design
- ♿️ Accessibility built-in
- 🌙 Dark mode support
- 🖨️ Print-friendly styles
- 🚫 No JavaScript required
- 🎨 Easy to customize

### Additional Features (Demonstrated Here)
- 📑 Multiple page support with navigation
- ✍️ Blog post support
- 📰 RSS feed for blog posts

## See It In Action
- View the [live demo](https://christophera.github.io/BaseTheme-DemoSite/)
- See [BaseTheme](https://github.com/ChristopherA/BaseTheme) for core foundation
- Full template files in this repository

## Quick Start

1. Use GitHub's "Use this template" button to create your repository
2. Edit `_config.yml`:
    ```yaml
    # Theme Settings
    remote_theme: "ChristopherA/BaseTheme@main"
    
    # Core Plugins (from BaseTheme - do not remove these)
    plugins:
      - jekyll-remote-theme         # Required for remote themes
      - jekyll-seo-tag             # Required for SEO meta tags
      - jekyll-sitemap             # Required for search engines
      - jekyll-titles-from-headings # Required for automatic page titles
      - jekyll-default-layout      # Required for automatic layouts
    
    # Optional Plugins (remove these if you don't use them)
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
├── _pages/             # Static pages
│   ├── about.md        # Example page
│   └── blog.md         # Blog index page
├── _posts/             # Blog posts
│   └── YYYY-MM-DD-*.md # Post files
└── index.md            # Home page
```

## Front Matter Reference

Required only for blog posts:
```yaml
---
date: YYYY-MM-DD   # Date required for blog posts
---
```

Common optional front matter:
```yaml
---
description: "SEO description"  # Optional: recommended for SEO
permalink: /custom-url/         # Optional: custom URL path
title: "Override Title"         # Optional: only if different from first heading
---
```

## Creating Content

BaseTheme automatically handles front matter for you, so you can focus on writing content:

### Static Pages
Create pages in `_pages/`:
```markdown
---
description: "About this site"  # Optional but good for SEO
permalink: /about/            # Optional - defaults to filename-based path
---
# About This Site

Welcome to my site!
```

### Blog Posts
Add posts in `_posts/`:
```markdown
---
description: "Introduction"  # Optional but good for SEO
date: 2024-11-21           # Required for blog posts
---
# My First Post

Hello world!
```

### Page Layout Types

Pages automatically get the right layout based on their location:
- Files named `index.md` → `home` layout
- Files in `_posts/` → `post` layout
- Other `.md` files → `page` layout
- `.html` files → `default` layout

## Local Development

While most users can rely on the free GitHub Pages infrastructure, you can optionally run Jekyll locally:

SIDENOTE: Most users do not need to run Jekyll locally - GitHub Pages will automatically build and serve your site.

If you do want to run locally, install Ruby and Jekyll for your operating system:
- macOS: `brew install ruby jekyll`
- Ubuntu/Debian: `sudo apt install ruby-full jekyll`
- Windows: See [Jekyll on Windows](https://jekyllrb.com/docs/installation/windows/)

Then run:
```zsh
bundle install   # Install required gems
jekyll serve     # Start local server at http://localhost:4000
```

More details are available at the official [Jekyll Installation Guide](https://jekyllrb.com/docs/installation/).

## License

Released under [CC0](LICENSE) ("No Rights Reserved"). Use freely without attribution.

## Author

Created by Christopher Allen ([GitHub @ChristopherA](https://github.com/ChristopherA))
