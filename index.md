---
layout: default
title: Home
---

# Welcome to My Site

A demonstration of minimal Jekyll website using BaseTheme as a remote-theme.

# Welcome to {{ site.title }}

{{ site.description }}

---

## Recent Posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small>— {{ post.date | date: "%B %d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
