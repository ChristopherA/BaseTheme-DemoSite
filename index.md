---
description: "A demonstration and template site showing how to build upon BaseTheme's lean foundation"
---

# Welcome to BaseTheme Demo

A demonstration site built using [BaseTheme](https://github.com/ChristopherA/BaseTheme) - a minimal Jekyll remote theme for GitHub Pages. While BaseTheme provides a lean foundation, this demo site shows you how to build upon that foundation for both simple web pages and optional features like blogs.

Think of BaseTheme as your starting point - a foundational building block. This demo site shows you how to add additional blocks together for a complete lean website, whether you need:
- 🪶 Basic web pages with clean navigation
- 📝 Blog posts with proper formatting
- 🔍 SEO-friendly metadata
- 📱 Mobile-first responsive design
- 🌙 Dark mode support
- 🖨️ Print-friendly styles
- 🎨 Easy customization options
- 🚫 No JavaScript requirements

[View Demo Site Source & Documentation](https://github.com/ChristopherA/BaseTheme-DemoSite)

## Recent Posts

{% for post in site.posts limit:3 %}
- <time class="post-date" datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date: site.date_format | default: "%B %d, %Y" }}</time> [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}

{% if site.posts.size > 3 %}
[View all posts]({{ '/blog/' | relative_url }})
{% endif %}

## Pages

{% include page_list.html %}
