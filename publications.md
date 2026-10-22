---
layout: page
title: Publications
permalink: /publications/
---

{%- assign pubs = site.publications | sort: "year" | reverse -%}
<ul class="pub-list">
{%- for pub in pubs -%}
  <li class="pub-item">
    <div class="pub-info">
      <h3 class="pub-title">{{ pub.title }}</h3>
      <p class="pub-authors">{{ pub.authors | join: ", " }}</p>
      <p class="pub-venue"><em>{{ pub.venue }}</em>, {{ pub.year }}</p>
    </div>
    <div class="pub-buttons">
      <a class="btn" href="{{ pub.url | relative_url }}">Abstract & Video</a>
      {%- if pub.doi -%}
      <a class="btn" href="{{ pub.doi }}" target="_blank" rel="noopener">Read Paper</a>
      {%- endif -%}
    </div>
  </li>
{%- endfor -%}
</ul>