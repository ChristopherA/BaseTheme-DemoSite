---
permalink: /blog/
description: "All blog posts"
---
# Blog Posts

{% for post in site.posts %}
## [{{ post.title }}]({{ post.url | relative_url }})

{{ post.date | date: site.date_format | default: "%B %d, %Y" }}

{{ post.excerpt }}

[Read more]({{ post.url | relative_url }})

---
{% endfor %}