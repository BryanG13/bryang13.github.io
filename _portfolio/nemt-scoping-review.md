---
title: "Non-emergency medical transportation planning: A systematic scoping literature review"
collection: portfolio
category: research
permalink: /project/2026-nemt-scoping-review
excerpt: "A PRISMA-based scoping review of 81 operations research studies on planning non-emergency medical transportation, extracted with a reproducible three-LLM pipeline, which shows how far the field still is from operational reality."
date: 2026-05-01
period: "2025 – 2026"
institution: "University of Antwerp (ANT/OR group)"
role: "Postdoctoral Researcher"
links:
  - label: "ANT/OR research group"
    url: "https://www.uantwerpen.be/en/research-groups/ant-or/"
---

Non-emergency medical transportation (NEMT) plans recurring, appointment-driven trips for patients and for healthcare equipment such as dialysis, chemotherapy and rehabilitation, as well as flows between and within hospitals. It should be a solved problem by now — it is a routing and scheduling problem with textbook structure, and a commercial software market exists. It is not. This review set out to establish exactly how much is actually known, and why the published methods still do not survive contact with an operations office.

**Screening.** The search followed **PRISMA 2020** across Web of Science and Scopus, identifying 741 records, removing 158 duplicates and screening 583 abstracts. Seventy-seven records met the abstract criteria, and manual searching and snowballing added 44 more. After removing further duplicates and 20 full-text exclusions, the final corpus is **81 studies** spanning 1996 to early 2026.

**Extraction.** Rather than extracting 81 papers by hand, each study was processed independently by **three large language models** (Claude Opus 4.6, o3 and Gemini 2.5 Pro) against a 27-field schema covering the research question, the optimization problem, the data used, the solution approach and the results. Of those, 23 categorical fields were scored against ground truth, giving **1,863 field comparisons** — 81 studies × 23 fields. The three models agree on 75.5% of fields, and accuracy averages **around 83%**, rising to 95.7% on the fields where all three agree. Every disagreement is flagged and adjudicated by two researchers independently, with a third breaking any tie; free-text similarity is judged with a word-level Jaccard threshold rather than by majority vote. The point is reproducibility: the extraction pipeline and the resulting dataset are released so the review can be re-run or extended.

**What the corpus shows.** The literature is concentrated on patient-centred routing models, and it is strikingly static: **63 of 81 studies are static, 20 dynamic and none dynamic-online**, while 76 of 81 assume a deterministic environment. Hard time windows appear in 56 studies. As for how these problems are solved, metaheuristics are the most common answer (33 studies), ahead of solver-based approaches (20), matheuristics (14), simple heuristics (13) and exact methods (11).

**Four gaps.** The synthesis identifies four interconnected gaps:

1. **Realism** — a persistent drift toward *simpler* models over time, with fewer heterogeneous fleets, less complex capacity and fewer multi-objective formulations in recent work than in older work.
2. **Solution methods** — custom exact methods are being abandoned in favour of calling a general-purpose MIP solver, leaving little that is specific to NEMT's own structure.
3. **Reproducibility** — only **16 of 81 studies released any artifact at all**, and only 13 of those links were still reachable when checked.
4. **Implementation** — **72 of 81 studies (88.9%) report no operational use**, with five active implementations, three planned and two pilots.

Written with **Kenneth Sörensen** (ANT/OR, University of Antwerp) and **Rafael A. Melo** (Institute of Computing, Federal University of Bahia). The manuscript has been submitted to *International Transactions in Operational Research* and is under peer review; the review was accepted as an oral presentation at CLAIO 2026.
