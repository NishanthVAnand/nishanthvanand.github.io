---
layout: page
title: Talks and Blogs
permalink: /posts/
background: /images/blog.jpg
---
<h2>Talks</h2>
<ul>
	<li>09/03/2019: Recurrent Value Functions, the RL sofa meeting, Mila. (<a href="https://www.youtube.com/watch?v=1HRA3wSCC3w">Youtube</a>)</li>
	<li>01/11/2019: Additive lambda returns, the RL sofa meeting, Mila. (<a href="https://www.youtube.com/watch?v=FchhKuo7NZE">Youtube</a>)</li>
	<li>22/01/2020: Dynamic programming, COMP 767, McGill University.</li>
	<li>15/04/2020: Q-learning and DQN, Guest lecture, PESU.</li>
</ul>
<h2>Blogs</h2>
<ul>
  {% for post in site.posts %}
    <li>
      <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
      <p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul>