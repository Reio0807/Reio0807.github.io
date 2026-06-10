---
layout: page
title: reading log
permalink: /reading/
nav: false
description: An annotated log of papers and posts I'm reading as I learn the field — short takes, not summaries.
---

Notes-in-public. For each piece I read closely, a few sentences on what it argues, why it matters,
and how it connects to the AI&nbsp;×&nbsp;economics-for-safety thread I'm pulling on. This is a
working log, not a polished bibliography — it's here to keep me honest about reading deeply rather
than just collecting links.

<div class="reading-list">
{% assign entries = site.reading | sort: "date" | reverse %}
{% for entry in entries %}
<div class="card mt-3 p-3">
  <h3 class="mb-1" style="font-size:1.15rem;">
    {% if entry.link %}<a href="{{ entry.link }}" target="_blank" rel="noopener">{{ entry.title }}</a>{% else %}{{ entry.title }}{% endif %}
  </h3>
  <p class="text-muted mb-2" style="font-size:0.85rem;">
    {% if entry.authors %}{{ entry.authors }}{% endif %}{% if entry.year %} · {{ entry.year }}{% endif %}{% if entry.date %} · read {{ entry.date | date: "%b %Y" }}{% endif %}
  </p>
  {{ entry.content }}
</div>
{% endfor %}
</div>
