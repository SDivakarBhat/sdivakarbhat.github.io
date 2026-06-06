---
layout: default
title: Writing
category: sample
permalink: /writing
redirect_from:
  - /posts
description: Essays on research, discipline, travel, fitness, dharma, and life between India and Japan.
---

<p>Occasional essays on research, discipline, travel, fitness, dharma, and life between India and Japan.</p>

  {% for post in site.posts %}
  <article>
    <h2>
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h2>
    <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date_to_long_string }}</time>
    <img src="{{ site.baseurl }}/assets/img/{{ post.image }}" width="auto" width="100%">
    {% if post.content contains "<!-- more -->" %}
      {{ post.content | split:"<!-- more -->" | first % }}
      <div style="text-align:right;">
        <a href="{{ post.url }}" style="color:#000;"> Read More </a>
      </div>
    {% else %}
      {{ post.content }}
    {% endif %}
  {% endfor %}
