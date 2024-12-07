# BaseTheme-DemoSite

This is a demonstration and template site built using [BaseTheme](https://github.com/ChristopherA/BaseTheme). While BaseTheme provides a lean foundation for static sites on GitHub Pages, this DemoSite shows how to build upon that foundation, illustrating both basic usage for web pages and optional features such as blog posts.

Think of BaseTheme as your starting point - a foundational building block. This DemoSite shows you how to add additional blocks together for a complete lean website.

## Features

- 🪶 Minimal, no-bloat foundation, no JavaScript required
- ✍️ Write naturally - no YAML front matter needed
  - 📄 Page titles from first heading
  - 🎯 Automatic layout detection
- 🎨 Flexible styling options
  - 🌓 Dark mode support
  - 🖨️ Print-friendly layouts
- 🌐 Responsive and accessible by design
  - 📱 Mobile-first approach  
  - ♿️ WCAG compliance built-in
- 🔍 SEO-ready with metadata and sitemaps

### Additional Features (Demonstrated Here)
- 📑 Multi-page navigation
- 📰 Blog post support with RSS feed

## See It In Action
- View the [live demo](https://christophera.github.io/BaseTheme-DemoSite/)
- See [BaseTheme](https://github.com/ChristopherA/BaseTheme) for core foundation
- Full template files in this repository

## Quick Start

1. Use GitHub's "Use this template" button to create your repository
2. Customize `_config.yml` - change the required settings to match your site, and delete any optional sections (like blog and social media) that you don't need:
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

## Creating Content

### Static Pages
Add markdown files to the `_pages` directory with a level-one heading (# Title). The heading becomes the page title, and the layout is chosen automatically. No front matter is needed.

You can override any defaults by adding optional front matter:

```markdown
---
# All of these are optional - only add what you need
permalink: /custom-url/
title: "TOPIC" # overrides getting title from first level-one heading (# Title) 
description: "All about my topic"  # Shows in search results and social media
---

# All about my topic

Everything you needed to know about my topic.

```

### Blog Pages
Add markdown files named YYYY-MM-DD-title.md to the `_posts` directory with a level-one heading (# Title). The heading becomes the post title, and the layout is chosen automatically. The only required front matter is the date:

```markdown
---
date: 2024-01-01  # Required for blog posts
---

# My First Blog Post

Everything you wanted to know about my first post.
```

## Additional Details

### Page Types and Layouts

Files automatically get the right layout based on their location:
1. Files named `index.md` → `home` layout
2. Posts in `_posts/` → `post` layout
3. Other `.md` files → `page` layout
4. `.html` files → `default` layout

You can override any automatic layout by specifying it in front matter:
```yaml
---
layout: custom-layout
---
```

### Page URLs (Permalinks)

For pages in the `_pages` directory:
- If you specify a `permalink:` in the front matter, that exact URL path will be used
- If you don't specify a permalink, Jekyll will automatically create a URL based on the filename:
  - `_pages/about.md` becomes `/about/`
  - `_pages/topics/specific.md` becomes `/topics/specific/`

Blog posts automatically get URLs based on their filename pattern:
`_posts/YYYY-MM-DD-title.md` becomes `/YYYY/MM/DD/title/`

### Blog Index Page
If using blog features, the `_pages/blog.md` will list all posts:

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
