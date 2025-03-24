---
layout: page
title: Categories
permalink: /categories/
---

<h2>📂 分类列表</h2>

{% for category in site.categories %}
<details style="margin-bottom: 1em;">
  <summary>
    <strong>{{ category[0] }}</strong>（{{ category[1].size }} 篇文章）
  </summary>
  <ul style="margin-top: 0.5em;">
    {% for post in category[1] %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <span style="color: #999; font-size: 0.9em;">{{ post.date | date: "%Y/%m/%d" }}</span>
    </li>
    {% endfor %}
  </ul>
</details>
{% endfor %}
