# BaseTheme-DemoSite

A demonstration site showing how to use the BaseTheme as a Jekyll remote-theme for use with GitHub Pages. Perfect as a template for your own minimal Jekyll website with both web pages and posts.

## License

This demo site is released under [CC0](LICENSE) ("No Rights Reserved"). You can copy, modify, distribute and use the site content and configuration without attribution or permission. For more details, see the [LICENSE](LICENSE) file.

## Author

Created by Christopher Allen ([GitHub @ChristopherA](https://github.com/ChristopherA) | ChristopherA@LifeWithAlacrity.com)

## Demo

See this template in action: [Live Demo](https://christophera.github.io/BaseTheme-SiteDemo/)

## Using This Template

1. Use the GitHub "Use this template" button to create your own repository, or manually copy these files to a new repository.

2. Update `_config.yml` with your settings:
   ```yaml
   # Theme Settings
   remote_theme: "ChristopherA/BaseTheme@main"
   plugins:
     - jekyll-remote-theme  # Required for remote theme

   # Site Settings
   title: "Your Site Title"
   description: "Your site description"
   url: "https://yourusername.github.io"
   baseurl: "/your-repo-name"

   # Optional Settings
   navigation:
     - title: Home
       url: /
     - title: About
       url: /about/
   date_format: "%B %d, %Y"

   # Jekyll Settings
   markdown: kramdown
   collections:
     pages:
       output: true
   ```

3. Edit the content:
  - Modify `index.md` for your home page
  - Update `pages/about.md` for your about page
  - Add posts in `_posts/` directory
  - Delete the sample post or use it as a template

4. Deploy to GitHub Pages:
  - Push your changes to your repository
  - Enable GitHub Pages in your repository settings

For more detailed instructions or to start from scratch instead of using this template, see the [BaseTheme README](https://github.com/ChristopherA/BaseTheme).
