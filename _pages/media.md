---
layout: page
title: media
permalink: /media/
nav: false
description: Podcasts, newsletters, and talks that shape how I think about AI safety and the economics of AI.
---

The inputs I keep coming back to. Podcasts for understanding how researchers and lab leadership
actually reason; newsletters for staying current without drowning. Listed roughly in the order I'd
recommend them to someone starting out.

<div class="media-list">
{% assign items = site.media | sort: "importance" %}
{% for item in items %}
<div class="card mt-3 p-3">
  <div class="d-flex justify-content-between align-items-baseline" style="gap:0.5rem; flex-wrap:wrap;">
    <h3 class="mb-0" style="font-size:1.15rem;">
      {% if item.link %}<a href="{{ item.link }}" target="_blank" rel="noopener">{{ item.title }}</a>{% else %}{{ item.title }}{% endif %}
    </h3>
    <span class="text-muted" style="font-size:0.8rem; text-transform:uppercase; letter-spacing:0.05em;">{{ item.medium_type }}</span>
  </div>
  {% if item.host %}<p class="text-muted mb-1" style="font-size:0.85rem;">{{ item.host }}</p>{% endif %}
  <p class="mb-0">{{ item.description }}</p>
</div>
{% endfor %}
</div>
