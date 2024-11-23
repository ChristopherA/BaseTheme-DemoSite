# BaseTheme-DemoSite

This is a demonstration and template site built using [BaseTheme](https://github.com/ChristopherA/BaseTheme). While BaseTheme provides an essential, lean foundation for static sites on GitHub Pages, this DemoSite shows how to build upon that foundation, illustrating both basic usage and optional features like blog posts.

Think of BaseTheme as your starting point - the essential building blocks. This DemoSite shows you how to put those blocks together into a complete website.

## Features

### Core Features (From BaseTheme)
- 🪶 Minimal, no-bloat foundation
- 🔍 SEO-friendly metadata
- 🗺️ Search engine sitemap
- 📱 Mobile-first responsive design
- ♿️ Accessibility built-in
- 🌙 Dark mode support
- 🖨️ Print-friendly styles
- 🚫 No JavaScript required
- 🎨 Easy to customize

### Additional Features (Demonstrated Here)
- 📝 Automatic page layouts (reduces front matter boilerplate)
- 📖 Automatic page titles from headings
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
      - jekyll-remote-theme    # Required for remote themes
      - jekyll-seo-tag        # Required for SEO meta tags
      - jekyll-sitemap        # Required for search engines

    # Optional Plugins (remove these if you don't use them)
      - jekyll-titles-from-headings  # Optional - auto-detects titles from content
      - jekyll-default-layout     # Optional - removes need for layout in front matter
    
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
│   ├── about.md        # Example page (remove if not using)
│   └── blog.md         # Blog index page (remove if not using blog)
├── _posts/             # Blog posts (remove if not using blog)
│   └── YYYY-MM-DD-*.md # Post files
└── index.md            # Home page
```

## Front Matter Reference

Required only for posts:
```yaml
---
date: YYYY-MM-DD   # Date required for blog posts
---
```

Common optional front matter:
```yaml
---
description: "SEO description"  # Optional: recommended for SEO
permalink: /custom-url/         # Optional: custom URL path, otherwise the file name
title: "Override Title"         # Optional: Only needed if different from first H1
---
```
For both web pages and posts:
- At least one markdown header  in the page content required unless you add a `title:` to the front matter.


## Creating Content`#`

### Static Pages (Optional)
Create pages in `_pages/` (remove directory if only using home page):
```yaml
---
description: "About this site"  # Optional but good for SEO
permalink: /about/            # Optional - defaults to filename-based path
---
# About This Site

Welcome to my site!
```

### Blog Posts (Optional)
If you want a blog, add posts in `_posts/` (remove directory if not using blog):
```yaml
---
description: "Introduction"  # Optional but good for SEO
date: 2024-11-21           # Required for blog posts
---
# My First Post

Hello world!
```

Note: The layout will be automatically set based on the file location - posts get the 'post' layout, other pages get the 'default' layout.

### Page and Post Titles

Thanks to the `jekyll-titles-from-headings` plugin, you don't need to specify a title in your front matter. The title will be automatically taken from the first header `#` (H1) in your content. For example:

```yaml
---
description: "About this site"  # Optional but good for SEO
permalink: /about/
---
# About This Site

Welcome to my site!
```

The title "About This Site" will be automatically used as the page title. Only add `title:` to your front matter if you want to override the H1 header, such as:

```yaml
---
title: "Different Title Than Header"  # This will override the H1 below
description: "About this site"
permalink: /about/
---
# About This Site

Welcome to my site!
```

In this case, "Different Title Than Header" will be used as the page title instead of "About This Site".

### Page URLs (Permalinks)

For pages in the `_pages` directory:
- If you specify a `permalink:` in the front matter, that exact URL path will be used
- If you don't specify a permalink, Jekyll will automatically create a URL based on the filename:
  - `_pages/about.md` becomes `/about/`
  - `_pages/topics/specific.md` becomes `/topics/specific/`

Blog posts automatically get URLs based on their filename pattern:
`_posts/YYYY-MM-DD-title.md` becomes `/YYYY/MM/DD/title/`

### Blog Index Page (Optional)
If using blog features, there is a `_pages/blog.md` that will list all posts (remove file if not using blog):

This will create a blog index page that:
- Lists all posts chronologically (newest first)
- Shows each post's title, date, and first paragraph
- Provides a link to the full post

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