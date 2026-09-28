---
title: "Packaging optimization at Atlas Copco"
collection: portfolio
category: industry
permalink: /project/2018-atlas-copco-packaging
excerpt: "Documenting the existing packaging policy for Atlas Copco's AIRnet and piping components, then optimizing it with a mixed-integer model and metaheuristics, with the aim of halving annual distribution and storage costs."
date: 2019-04-01
period: "2018 – 2019"
institution: "Atlas Copco, Wilrijk (Belgium)"
role: "Young talent programme participant, then Improvement Consultant"
---

Packaging is one of those costs that never gets measured properly. It sits between manufacturing and logistics, it is decided in a dozen different places, and nobody owns the total. Atlas Copco's young talent programme gave me a two-month window to find out what the packaging policy actually was, and then a consulting stint to follow through.

**Documenting.** The first job was to establish the reality: which packaging configurations were used for which items, and what the existing policy was in practice rather than in theory. That baseline is the only thing that makes an optimization result mean anything, and it was more work than the modeling.

**Optimizing.** With the baseline in hand, I built a **mixed-integer model that assigns a packaging option to each item**, subject to the physical and commercial constraints each option implies. The interesting part was not the formulation but the constraints themselves: they came from weekly meetings with people in different departments, each of whom knew about a restriction that did not appear in any specification. Packaging design candidates were then generated with **metaheuristics, such as simulated annealing**, rather than enumerated by hand.

The objective was to cut annual distribution and storage costs, currently dominated by the volume and the number of handling steps, by roughly half, and the engagement ended with an implementation plan rather than a slide deck.

**Following through.** I then continued as an improvement consultant, documenting the packaging policy for piping components and proposing where it could be standardised. The most transferable finding was that packaging decisions are *postponable*: where a component is packed identically at several stages, a decision made early can be pushed to the last moment and chosen from actual demand. That same idea turned up independently in a supply chain audit I later ran, and it is the kind of thing you only notice once you have seen both sides of it.
