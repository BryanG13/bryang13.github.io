---
title: "Designing a system for parts picking and line supply"
collection: portfolio
category: coursework
permalink: /project/2018-production-facility-design
excerpt: "Designing a greenfield plant for a manufacturer of 21,000 electric golf carts a year: takt time and line balancing for a high-customization line, a kitting supermarket for parts supply, the facility layout, and a discrete-event simulation to check the whole thing holds together."
date: 2018-06-01
period: "2018"
institution: "Ghent University (Design of Manufacturing and Service Operations)"
role: "Team project, supervised by Prof. Birger Raa and Prof. Dieter Claeys"
---

A new entrant in the electric golf cart market asked us to design its production facility from scratch. The reports deliberately keep the company anonymous, so I will keep it that way, but everything else is real: **15,000 long and 6,000 short carts a year**, 21,000 in total, on two 8-hour shifts over 200 working days, with a *single* assembly line expected to absorb heavy customization.

That last point is what makes it hard. Variety on one line means takt time has to be set by the worst-case variant, or everything else on the line ends up waiting.

**Takt time and allowances.** The raw takt time works out at 8.57 minutes per cart. Applying the standard 12% allowances for fatigue and the unavoidable gives a workable cycle of **7.54 minutes**.

**Line balancing.** Rather than hand-balancing, we wrote our own line-balancing heuristic in Python (an improved upstream-first approach, ranking tasks by reverse positional weight) and scored the candidate configurations with the **Smoothness Index** and **Line Efficiency**. The best configuration balanced 24 workstations (21 on the main line, plus two and one for sub-assembly) with a Smoothness Index of 11.18 and line efficiency of 78.96%, along with two dedicated engine-mounting stations.

**Parts supply.** How the line gets fed turned out to matter as much as the line itself. Rather than a supermarket of thousands of individual parts, we designed a kitting operation building **85 kits**, with 17 kitting stations, 1,980 reusable containers, 13 forklifts and a single AGV, keeping work-in-process at 21 carts.

**Plant layout and validation.** Finally the layout, and then the part that decides whether any of it is real: a **FlexSim** discrete-event simulation of the whole facility. It gave kitting capacity of about 72 kits per hour, an engine line running at 12.31 against 8.75 carts per hour on the fourth workstation, and an average lead time of 191 minutes.

The first simulation run produced 19,282 carts against the 21,000 target, 1,718 short. That gap is exactly the kind of thing a project like this exists to find out, and it fed straight back into the design decisions.
