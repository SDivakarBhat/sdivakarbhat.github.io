---
layout: default
title: Posts
category: sample
permalink: /posts
---
<ul>
  {% for post in site.posts %}
    {% if post.content contains "<!-- more -->" %}
      {{ post.content | split:"<!-- more -->" | first % }}
      <div style="text-align:right;">
        <a href="{{ post.url }}" style="color:#000;"> Read More </a>
      </div>
    {% else %}
      {{ post.content }}
    {% endif %}
  {% endfor %}
</ul>
