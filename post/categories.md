---
layout: default
title: "Categories are"
---

# 1
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

# 2

{% for cate in site.category %}
<article>
  <h1 id="{{ cate }}">{{ cate }}</h1>
  <ul>
    {% for post in cate %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
</article>
{% endfor %}

# 3
{% for category in site.categories %}
    <a href="/category/{{ category[0] }}.html" style="text-decoration: none;">{% if category[0] == 'eem' %}{{ category[0] | upcase }}{% else %}{{ category[0] | capitalize }}{% endif %}</a><br />
{% endfor %}

