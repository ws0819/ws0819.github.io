---
layout: page
title: 제목쓰는곳
permalink: /about/
---
<div class="archive">
  {% for post in site.posts %} {% assign currDate = post.date | date: "%Y" %} {%
  if currDate != date %}
  <h1 class="archive-year">{{ currDate }}</h1>
  {% assign date = currDate %} {% endif %}
  <div class="archive-item">
    <span class="post-date archive-date fs-4"
      >{{ post.date | date: "%B %d, %Y" }}</span
    >
    <a href="{{ post.url | relative_url }}" class="archive-title fs-4"
      >{{ post.title }}</a
    >
  </div>
  {% endfor %}
</div>