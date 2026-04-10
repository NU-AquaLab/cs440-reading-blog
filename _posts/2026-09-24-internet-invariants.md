---
layout: post
title: "What Can We Actually Rely On About the Internet?"
date: 2026-09-24
paper_authors: "C. Misa, W. Willinger, R. Durairajan, R. Rejaie"
paper_venue: "NINeS 2026"
paper_url: "https://nines-conference.org/papers/p022-Misa.pdf"
week: 1
tags: [architecture, invariants, traffic, self-similarity]
---

## Key Idea

Certain statistical properties of Internet traffic — self-similar scaling in time, multifractal scaling of IP addresses in space — have held for 30 years, but nobody has explained *why*. This paper proposes a three-part framework: reproducible evidence, a generative model grounded in real mechanisms, and an architectural justification using Highly Optimized Tolerance (HOT). The core claim is that these invariants are not emergent accidents but signatures of deliberate design trade-offs.

## Critique

The framework is intellectually clean, but the paper acknowledges it is work-in-progress — HOT is shown to *plausibly* explain the invariants, not proven to be the right (or only) lens. Self-organized criticality is dismissed quickly; a head-to-head comparison on the same data would be more convincing. Still, the reverse-engineering framing is genuinely useful: if we know *why* an invariant holds, we can predict when it will break.

## Connections

This is the first post — no backward links yet. But I expect the HOT framing to resurface when we discuss congestion control (Week 4) and datacenter transport (Week 5). If self-similarity comes from how users consume content, what happens when the traffic mix shifts to ML training workloads?

*I will update this section as the quarter progresses.*
