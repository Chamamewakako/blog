---
layout: default
title: Home
---

<ul class="post-list">
{% for post in site.posts %}
  <li class="post-list-item">
    <span class="post-list-date">{{ post.date | date: "%Y年%m月%d日（%a）" }}</span>
    <div class="post-list-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></div>
    <p class="post-list-excerpt">{{ post.excerpt | strip_html | remove: "目次を開く" | truncate: 80 }}</p>
  </li>
{% endfor %}
</ul>
