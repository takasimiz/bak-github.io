---
layout: default
title: "Categories are"
---

{% for cate in site.category %}
<article>
  <h1 id="cate_{{ cate[0] }}">{{ cate[0] }}</h1>
  <ul>
    {% for post in cate[1] %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
</article>
{% endfor %}
