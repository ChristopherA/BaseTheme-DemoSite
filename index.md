---
layout: default
title: Home
---

# Welcome to {{ site.title }}

{{ site.description }}

[About {{ site.title }}](/about/)

---

## Pages

{% include page_list.html %}

## Posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small>— {{ post.date | date: site.date_format | default: "%B %d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
