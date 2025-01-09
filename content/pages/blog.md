---
title: Blog
description: "Update from Blog Article"
pagination:
  data: collections.posts
  size: 4
  reverse: true
testdata:
 - item1
 - item2
permalink: "blog/{% if pagination.pageNumber > 0 %}page-{{ pagination.pageNumber + 1 }}/{% endif %}index.html"
---
<ul>
{%- for post in pagination.items %}
<li>
<h3><a href="{{ post.url }}" class="postlist-link">{{ post.data.title }}</a></h3>
<p>{{post.data.description}}</p>
</li>
{% endfor %}
</ul>

