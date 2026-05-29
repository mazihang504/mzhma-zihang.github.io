---
layout: default
---

<h1>博客文章</h1>

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <span class="post-meta">{{ post.date | date: "%Y年%m月%d日" }}</span>
      <p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul>

{% if site.posts.size == 0 %}
  <p>暂无文章，敬请期待！</p>
{% endif %}
