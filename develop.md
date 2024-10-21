---
layout: develop
title: 개발일지
permalink: /develop/
---
<div class="archive">
  {% for develop in site.develops %} {% assign currDate = develop.date | date: "%Y" %} {%
  if currDate != date %}
  <h1 class="archive-year">{{ currDate }}</h1>
  {% assign date = currDate %} {% endif %}
  <div class="archive-item">
    <span class="develop-date archive-date fs-4"
      >{{ develop.date | date: "%B %d, %Y" }}</span
    >
    <a href="{{ develop.url | relative_url }}" class="archive-title fs-4"
      >{{ develop.title }}</a
    >
  </div>
  {% endfor %}
</div>