---
layout: page
title: Multi-agent "AI scientist" systems for development economics
description: Multi-agent LLM systems that design and iterate field-experiment nudges, with causal evaluation of AI vs. human treatments.
importance: 1
category: research
---

As a pre-doctoral researcher with Prof. David Yanagizawa-Drott, I build multi-agent LLM systems
that act as automated "scientists" — proposing behavioral nudges for field experiments, simulating
how people might respond, and iterating on their own designs. The work spans:

- **Multi-agent design loops** — separate LLM agents that propose, critique, and refine
  field-experiment treatments.
- **Causal evaluation** — estimating effects with ITT/OLS, robust standard errors, and CATE to
  benchmark AI-designed treatments against human-designed ones.
- **Behavioral surrogates** — LLM-simulated personas plus embedding + gradient-boosting models that
  approximate human behavior.
- **Self-improving agents** — chatbots optimized via contextual bandits and prompt search.

**Why it matters for safety:** these are exactly the kinds of multi-agent, self-improving systems
whose failure modes — reward hacking, miscalibration, emergent strategic behavior — the safety
community studies. Building them gives me a concrete, hands-on view of where they break, and where
evaluation and oversight need to live.
