---
layout: mypost
title: Links
---

# 友链页面

<ul>
  {%- for link in site.data.links %}
  <li>
    <a href="{{ link.url }}" target="_blank" >{{ link.title }}</a><p align="right">{{ link.describe }}</p>
  </li>
  {%- endfor %}
</ul>
