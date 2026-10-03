---
layout: page
permalink: /press/
title: press
description: Work mentions and media coverage
nav: true
nav_order: 2
---

<!-- _pages/press.md -->
<div class="press">
{% for item in site.data.press %}
  <div class="row press-item">
    <div class="col-sm-2">
      <p class="press-year">{{ item.date | split: " " | last }}</p>
    </div>
    <div class="col-sm-3 text-sm-right">
      <p class="press-outlet">{{ item.outlet }}</p>
    </div>
    <div class="col-sm-7">
      <p><a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">{{ item.title }}</a></p>
      {% if item.related %}
      <p class="press-related">Related work: {{ item.related }}</p>
      {% endif %}
    </div>
  </div>
  {% unless forloop.last %}<hr>{% endunless %}
{% endfor %}
</div>
