---
layout: default
permalink: /blog/
description: "All blog posts"
---
# Blog Posts

{% assign posts = site.posts %}
{% for post in posts %}
## [{{ post.title }}]({{ post.url | relative_url }})

<time class="post-date" datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date: site.date_format | default: "%B %d, %Y" }}</time>

{{ post.excerpt }}

[Read more]({{ post.url | relative_url }})

---
{% endfor %}
