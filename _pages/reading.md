---
layout: page
title: reading & workshop notes
permalink: /reading/
nav: false
description: "Notes from papers, books, and workshops as I explore AI safety and economics."
---

Notes-in-public from what I'm reading and learning. The reading log holds short reflections;
the workshop notes are longer, organized references with practical takeaways and source details.

<h2 id="workshop-notes">Workshop notes</h2>

<div class="card mt-3 p-3">
  <h3 class="mb-1" style="font-size:1.15rem;">
    <a href="{{ '/notes/spar-research-with-agents/' | relative_url }}">Doing better research with AI agents</a>
  </h3>
  <p class="text-muted mb-2" style="font-size:0.85rem;">SPAR Fellowship workshop · Yoav Tzfati · September 30, 2026</p>
  <p>How to delegate substantial research tasks, communicate intent, retrieve useful context, and review agent-generated work. Includes a delegation ladder, timestamped explanations, debrief checklists, and reusable prompts.</p>
  <p>Compiled from my notes, workshop slides, and an Otter export with AI assistance. Transcript-supported points, summary-only material, and added interpretations are labeled separately.</p>
  <p class="mb-0"><a href="{{ '/notes/spar-research-with-agents/' | relative_url }}">Read the full workshop notes →</a> <span class="text-muted">· Print / save as PDF from the note</span></p>
</div>

## Reading log

For each piece I read closely, a few sentences on what it argues, why it matters, and how it
connects to AI and economics. This is a working log, not a polished bibliography.

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
