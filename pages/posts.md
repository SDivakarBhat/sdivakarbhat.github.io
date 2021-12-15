---
layout: default
title: Posts
category: sample
permalink: /posts
---
{% for post in paginator.posts %}
  {% include featured-post.html %}
{% endfor %}
