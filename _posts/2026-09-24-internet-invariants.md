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

## Problem

The Internet changes constantly — new applications, new protocols, new
infrastructure — yet certain statistical properties of its traffic have held
steady for 30 years. Self-similar (temporal) scaling of link traffic and
multifractal (spatial) scaling of observed IP addresses keep showing up in
measurements regardless of where or when you look. The networking community
has treated these as empirical curiosities, but never satisfactorily explained
*why* they persist. Without that explanation, we cannot know whether they are
durable foundations to build on or coincidences that will eventually break.

## Key Idea

The paper proposes a three-part framework for turning an observed invariant
into an *understood* one:

1. **Reproducible empirical evidence** that the statistical behavior exists.
2. **A generative model** grounded in concrete network mechanisms (not just
   curve fitting) that explains *how* the behavior arises.
3. **An architectural justification** — using Highly Optimized Tolerance
   (HOT) — that explains *why* the underlying mechanisms exist as outcomes
   of robust design under constraints.

They apply this to multifractal scaling of IP addresses in traffic traces,
proposing a finite conservative cascade model tied to how addresses are
actually allocated and used. The core argument: these invariants are not
emergent accidents but visible signatures of deliberate (if implicit) design
trade-offs.

## Evaluation

This is a framework paper, so the "evaluation" is more conceptual than
experimental. They revisit earlier empirical findings on multifractal address
structure and reframe them through their three-part lens. The paper is upfront
that this is work-in-progress — they call their results "preliminary" and
acknowledge that HOT is not proven to be the *only* valid architectural lens.

The strength is intellectual honesty: they explicitly state what they have not
yet shown and invite alternatives. The weakness is that without a competing
framework to compare against, it is hard to judge how much explanatory power
HOT actually adds versus simply being a plausible narrative.

## Critique

The most provocative claim is that Internet invariants are *designed* outcomes
rather than emergent phenomena. This is a strong ontological position, and the
paper does not fully close the argument. They show that HOT *can* explain the
invariants, but "can explain" is weaker than "does explain." Self-organized
criticality (SOC) is dismissed somewhat quickly — a more careful comparison
with SOC-based explanations on the same data would strengthen the case.

I also wonder about scope. The paper restricts itself to wide-area Internet
traffic and explicitly excludes datacenters and industrial networks. But if
the framework is about architectural design principles, shouldn't it say
something about environments where those principles differ? The absence of
invariants in a datacenter could be just as informative as their presence on
backbone links.

That said, the reverse-engineering / forward-engineering framing is genuinely
useful. If we can identify *why* an invariant holds, we can predict when it
will *stop* holding — which is exactly what network designers need.

## Connections

This is the first post in my reading blog, so no backward links yet. But I
expect the HOT framing — invariants as optimization outcomes — to resurface
when we discuss congestion control (Week 4) and datacenter transport (Week 5).
If self-similarity in traffic traces is a consequence of how users consume
content, what happens when the traffic mix shifts to ML training workloads
that look nothing like web browsing?

*I will update this section as the quarter progresses.*

## Takeaway

"Internet invariant" should not mean "interesting pattern we keep measuring."
It should mean: we know why it is there, what design choices sustain it, and
under what conditions it would disappear. This paper starts building that
stronger definition.
