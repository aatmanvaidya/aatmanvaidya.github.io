---
layout: page
permalink: /press/
title: press
description: Work mentions and media coverage
nav: true
nav_order: 2
---

<!-- _pages/press.md -->
<div class="table-responsive">
  <table class="table table-sm table-borderless">
  {% for item in site.data.press %}
    <tr>
      <th scope="row" style="white-space: nowrap">{{ item.date }}</th>
      <td>
        <b>{{ item.outlet }}</b> on <a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">&ldquo;{{ item.title }}&rdquo;</a>
      </td>
    </tr>
  {% endfor %}
  </table>
</div>
