---
layout: default
title: Tags
---

<h1> Tags </h2>

{% for tag in site.tags %}
<article>
  <h2 id="tag_{{ tag[0] }}">{{ tag[0] }}</h2>
  <ul>
    {% for post in tag[1] %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
</article>
{% endfor %}
