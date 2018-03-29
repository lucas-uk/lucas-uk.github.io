---
layout: page_ver2
title: All blog posts
---

<div>
<ul>
    {% for post in site.posts %}
      <li><span>{{ post.date | date: "%Y-%m-%d" }} &raquo; </span><a href="{{ post.url }}">{{ post.title }}</a>
	  {{ post.excerpt }}
	  </li>
    {% endfor %}
</ul>
</div>

