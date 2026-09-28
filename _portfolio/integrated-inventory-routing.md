---
title: "An integrated inventory and routing problem"
collection: portfolio
category: coursework
permalink: /project/2016-integrated-inventory-routing
excerpt: "A home-care distributor had to decide whether to keep delivering in-house or outsource, and from which of two depots — a periodic inventory and routing model over a 12-week cycle, with service level verified by Monte Carlo."
date: 2016-12-01
period: "2016"
institution: "Ghent University — Operations Research: Applications and Algorithms"
role: "Team project, supervised by Prof. E.-H. Aghezzaf and ir. R. Amaral"
---

AHP, a home-care distributor, supplies ten clients on a recurring 12-week planning cycle. Its own distribution system was too expensive and was missing its service level target, so the question was concrete: **redesign the single-location system, or outsource the whole thing to a 3PL?** And if in-house, which of the two depots should serve which clients?

**The model.** This is a periodic inventory and routing problem, formulated as a mixed-integer program in AMPL covering a single truck per period, with subtour elimination, depot-selection, periodicity and client-capacity constraints. Seven model versions went into it as the formulation was tightened.

**The answer.** Serving all ten clients from DC1 costs **€5,599.53** over the cycle, DC2 €5,604.63 — essentially identical. Outsourcing comes in at **€2,102.69** via DC1 and €2,113.57 via DC2. Outsource, and the depot choice barely matters: the 3PL is around **62% cheaper** than running the operation in-house, and the difference is not a rounding error in any direction.

**Where it gets interesting.** Service level was not something the model was allowed to assume away, so it was verified separately by **Monte Carlo simulation over 300 scenarios**. The baseline network served clients between **61.7% and 89.3%**, with the worst client at 61.7% — which is to say, badly under target. The levers that actually moved it:

- **more pallets per visit** took one client from 83% to 99.3% and another to 100%;
- **halving forecast variance** brought 9 of 10 clients to 95% or better;
- **raising client capacity** pushed every single client above 97%.

So the real finding was that service level is a function of *how often and how much you deliver*, not of where you deliver from. A second round of analysis tuned the replenishment frequencies directly to a 95% target, with one client still stuck at 62.3% no matter what — which, as far as I am concerned, is the most useful thing the model said.
