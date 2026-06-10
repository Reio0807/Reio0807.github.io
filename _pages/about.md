---
layout: about
title: about
permalink: /
subtitle: Pre-doctoral researcher in AI&nbsp;×&nbsp;economics, moving into AI safety · <strong>open to roles, fellowships &amp; collaborations</strong>.

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>Zurich, Switzerland</p>
    <p><a href="mailto:bbai02@berkeley.edu">bbai02@berkeley.edu</a></p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: true
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

<div class="bb-hero">
  <div class="bb-eyebrow">AI&nbsp;×&nbsp;ECONOMICS&nbsp;→&nbsp;AI&nbsp;SAFETY</div>
  <h1 class="bb-title">I work where <span class="bb-grad">economics</span> meets <span class="bb-grad">AI safety</span>.</h1>
  <div class="bb-typed-wrap"><span class="bb-arrow">&gt;</span>&nbsp;<span id="bb-typed"></span><span class="bb-cursor">▋</span></div>
  <div class="bb-cta">
    <a class="bb-btn bb-btn-primary" href="{{ '/compass/' | relative_url }}">Explore the Field Compass</a>
    <a class="bb-btn" href="{{ '/blog/' | relative_url }}">Read the blog</a>
    <a class="bb-btn" href="{{ '/assets/pdf/CV_Bohan_Bai.pdf' | relative_url }}" target="_blank" rel="noopener">CV (PDF)</a>
  </div>
  <div class="bb-chips">
    <span class="bb-chip">multi-agent LLM systems</span>
    <span class="bb-chip">causal inference</span>
    <span class="bb-chip">AI evaluations</span>
    <span class="bb-chip">mechanism design</span>
    <span class="bb-chip">the economics of AI</span>
  </div>
</div>

<style>
.bb-hero{
  /* hero accent palette — grayish-blue into a glittering sky blue */
  --bb-accent: #4f86c6;
  --bb-accent-2: #5ec2ff;
  margin: 0.5rem 0 2.2rem;
  padding-bottom: 1.6rem;
  border-bottom: 1px solid var(--global-divider-color);
  opacity: 0; transform: translateY(14px);
  animation: bb-rise .7s cubic-bezier(.2,.7,.2,1) .05s forwards;
}
.bb-eyebrow{
  font-family: ui-monospace, "SFMono-Regular", "JetBrains Mono", Menlo, Consolas, monospace;
  font-size: .72rem; letter-spacing: .18em; font-weight: 600;
  color: var(--bb-accent); opacity: .95; margin-bottom: .6rem;
}
.bb-title{
  font-size: clamp(1.7rem, 4.4vw, 2.65rem); line-height: 1.12; font-weight: 800;
  letter-spacing: -.01em; margin: 0 0 .7rem;
}
.bb-grad{
  background: linear-gradient(120deg, #6f8db3, var(--bb-accent) 48%, var(--bb-accent-2));
  -webkit-background-clip: text; background-clip: text;
  -webkit-text-fill-color: transparent; color: transparent;
}
.bb-typed-wrap{
  font-family: ui-monospace, "SFMono-Regular", "JetBrains Mono", Menlo, Consolas, monospace;
  font-size: .95rem; color: var(--global-text-color); opacity: .82;
  min-height: 1.5em; margin-bottom: 1.15rem;
}
.bb-arrow{ color: var(--bb-accent); font-weight: 700; }
.bb-cursor{ color: var(--bb-accent); animation: bb-blink 1.05s step-end infinite; }
.bb-cta{ display:flex; flex-wrap:wrap; gap:.55rem; margin-bottom:1.15rem; }
.bb-btn{
  display:inline-block; padding:.5rem .95rem; border-radius:9px;
  font-size:.86rem; font-weight:600; text-decoration:none;
  border:1px solid var(--global-divider-color);
  color: var(--global-text-color); transition: all .18s ease;
}
.bb-btn:hover{ border-color: var(--bb-accent); color: var(--bb-accent); transform: translateY(-1px); text-decoration:none; }
.bb-btn-primary{
  background: var(--bb-accent); color:#fff; border-color: var(--bb-accent);
}
.bb-btn-primary:hover{ color:#fff; opacity:.9; filter:brightness(1.05); }
.bb-chips{ display:flex; flex-wrap:wrap; gap:.45rem; }
.bb-chip{
  font-family: ui-monospace, "SFMono-Regular", "JetBrains Mono", Menlo, Consolas, monospace;
  font-size:.72rem; padding:.2rem .55rem; border-radius:6px;
  border:1px solid var(--global-divider-color);
  color: var(--global-text-color); opacity:.72;
}
@keyframes bb-rise{ to{ opacity:1; transform:none; } }
@keyframes bb-blink{ 50%{ opacity:0; } }
@media (prefers-reduced-motion: reduce){
  .bb-hero{ animation:none; opacity:1; transform:none; }
  .bb-cursor{ animation:none; }
}
</style>

<script>
(function(){
  var el = document.getElementById("bb-typed");
  if(!el) return;
  var phrases = [
    'pre-doctoral researcher in AI × economics',
    'building multi-agent "AI scientist" systems',
    'mapping a path into technical AI governance',
    'learning AI safety — in public'
  ];
  var reduce = window.matchMedia && window.matchMedia("(prefers-reduced-motion: reduce)").matches;
  if(reduce){ el.textContent = phrases[0]; return; }
  var p=0, c=0, deleting=false;
  function tick(){
    var word = phrases[p];
    el.textContent = word.substring(0, c);
    if(!deleting){
      if(c < word.length){ c++; setTimeout(tick, 42); }
      else { deleting=true; setTimeout(tick, 1700); }
    } else {
      if(c > 0){ c--; setTimeout(tick, 22); }
      else { deleting=false; p=(p+1)%phrases.length; setTimeout(tick, 320); }
    }
  }
  tick();
})();
</script>

I'm **Bohan Bai** — a pre-doctoral researcher with a background in economics, moving deliberately
toward **AI safety**. My training sits where economics meets machine learning: a B.A. in Economics with a CS minor from
**UC Berkeley**, an M.S. in Quantitative Management (Business Analytics) from **Duke (Fuqua)**, and
a pre-doctoral position building multi-agent LLM "**AI scientist**" systems for development economics
with Prof. David Yanagizawa-Drott in Zurich.

Day to day I work on things like LLM-simulated economic agents, causal estimation of treatment
effects (ITT/OLS, CATE), behavioral calibration of language models, and self-improving agentic
systems. That work has convinced me that the **economics of AI is not a side quest for AI safety —
it is part of the core**: incentives, mechanism design, evaluation, and the labor- and
market-level effects of increasingly capable agents all bear directly on whether advanced AI goes
well.

I'm still in an **exploration phase**, mapping the field across technical AI governance, AI policy,
and technical alignment — with a particular interest in **where AI × economics can contribute to
safety**: evaluations, multi-agent risk, mechanism design for AI-populated markets, and the
calibration and reliability of LLMs used for decision-making.

This site is my open record of that journey: **[writing](/blog/)** that works through ideas,
a **[field compass](/compass/)** mapping the AI-safety × AI-econ landscape, a curated set of
**[resources](/resources/)** and a **[reading log](/reading/)**, the **[media](/media/)** shaping my
thinking, the **[ideas and thinkers](/ideology/)** that influence me, and the
**[projects](/projects/)** I've built along the way. The **[now page](/now/)** says what I'm focused
on this month.

**I'm open to roles, fellowships, and collaborations** in AI safety, AI governance, and the economics
of AI. The best way to reach me is by [email](mailto:bbai02@berkeley.edu).
