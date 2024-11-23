# BaseTheme-DemoSite

A demonstration site showing how to use BaseTheme - a minimal Jekyll remote theme - for GitHub Pages. This demo includes both simple web pages and blog posts, plus examples of useful optional features you can add to your site.

## See It In Action

View this template live: [Demo Site](https://christophera.github.io/BaseTheme-DemoSite/)

For a minimal implementation without these additional features, see the [BaseTheme README](https://github.com/ChristopherA/BaseTheme).

## License

This demo site is released under [CC0](LICENSE) ("No Rights Reserved"). You can copy, modify, distribute and use the site content and configuration without attribution or permission.

## Author

Created by Christopher Allen ([GitHub @ChristopherA](https://github.com/ChristopherA) | ChristopherA@LifeWithAlacrity.com)

## Usage

### Basic Setup

1. Use the GitHub "Use this template" button to create your own repository, or manually copy these files to a new repository.

2. Add basic configuration to `_config.yml`:
    ```yaml
    # Theme Settings
    remote_theme: "ChristopherA/BaseTheme@main"
    plugins:
      - jekyll-remote-theme  # Required

    # Site Settings
    title: "Your Site Title"
    description: "Your site description"
    url: "https://yourusername.github.io"
    baseurl: "/your-repo-name"  # Leave empty if hosting at root URL
    ```

3. Deploy to GitHub Pages:
   - Push your changes to your repository
   - Enable GitHub Pages in your repository settings

### Content Creation

Create your site content:

- Modify `index.md` for your home page
- Create pages in `_pages/` directory with front matter:
    ```yaml
    ---
    layout: default
    title: "Page Title"
    description: "A brief description of this page"  # Optional but good for SEO
    permalink: /about/
    ---
    ```
- Add posts in `_posts/` directory with front matter 
    ```yaml
    ---
    layout: post
    title: "A Post"
    description: "Welcome!"  # Optional but good for SEO
    date: 2024-11-21
    ---
    ```
- NOTE: These `description` fields are optional but recommended for better search engine visibility.

### Features Beyond BaseTheme

This demo also shows how to enhance BaseTheme's minimal foundation with useful, low-overhead features. Each requires explicit inclusion in your `_config.yaml`. If you don't need them, you can remove them:

#### Enhanced Content Discovery

1. **RSS Feed** (`jekyll-feed`)
   - Automatically generates an RSS/Atom feed at `/feed.xml`
   - Great for allowing readers to subscribe to your posts
   - No additional configuration needed
    ```yaml
    plugins:
      - jekyll-feed
    ```

2. **SEO Tags** (`jekyll-seo-tag`)
   - Adds meta tags for search engines and social networks
   - Uses your `title`, `description`, and post metadata
   - No additional configuration needed
    ```yaml
    plugins:
      - jekyll-seo-tag
    ```

3. **Sitemap** (`jekyll-sitemap`)
   - Creates `sitemap.xml` for search engines
   - Automatically includes all your pages and posts
   - No additional configuration needed
    ```yaml
    plugins:
      - jekyll-sitemap
    ```

#### Content Organization

1. **Pagination** (`jekyll-paginate`)
   - Splits your post listing into pages
   - Recommended when you have more than ~10 posts
   - Requires additional configuration:
    ```yaml
    plugins:
      - jekyll-paginate
    paginate: 5  # Posts per page
    paginate_path: "/blog/page:num/"
    ```

2. **Navigation**
   - Customize the site menu structure
    ```yaml
    navigation:
      - title: Home
        url: /
      - title: About
        url: /about/
      - title: Blog
        url: /blog/
    ```

3. **Collections**
   - Organize related content (like pages) together
    ```yaml
    collections:
      pages:
        output: true
    ```

#### Date Formatting

Customize how dates appear throughout your site:
    ```yaml
    date_format: "%B %d, %Y"  # November 22, 2024
    # or
    date_format: "%Y-%m-%d"   # 2024-11-22
    ```
