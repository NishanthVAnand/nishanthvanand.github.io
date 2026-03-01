---
layout: page
title: Blog
---

<ul>
  {% for post in site.posts %}
    <li>
      <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
      <p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul>

<ul>
  <li class="blogs"> <b>February 2026:</b> <a style="color:blue;" href="https://itsnva7.substack.com/p/continual-learning-requires-rethinking">Continual Learning requires Rethinking Learning Architectures.</a></li>
</ul>