---
title: "Demand-responsive feeder services: from exact models to real-time heuristics"
collection: portfolio
category: phd
permalink: /project/2022-demand-responsive-feeder-services
excerpt: "The central research line of my PhD: designing a semi-flexible feeder bus service that sits between the predictability of a traditional route and the efficiency of a fully flexible on-demand service, together with the exact and heuristic methods needed to operate it."
date: 2022-05-01
period: "2019 – 2023"
institution: "University of Antwerp (PhD, joint with KU Leuven)"
role: "PhD researcher (first author)"
links:
  - label: "Networks (2022)"
    url: "https://doi.org/10.1002/net.22095"
  - label: "Transportation Research Part C (2021)"
    url: "https://doi.org/10.1016/j.trc.2021.103102"
  - label: "Transportmetrica A (2023)"
    url: "https://doi.org/10.1080/23249935.2023.2227738"
  - label: "IFORS 2023 talk"
    url: "/talks/2023-ifors"
---

A *feeder service* moves passengers from a low-demand area, typically suburban or rural, to a transportation hub, where they continue their journey on the regular network. Traditional feeder services are predictable and easy to control, but wasteful when demand is low or scattered. Fully flexible on-demand services are efficient, but unpredictable, harder to control financially, and they cannot serve passengers who do not reserve in advance.

The service studied here occupies a **Goldilocks zone** between the two. It is *semi-flexible*, and has two kinds of bus stops:

- **Mandatory stops** are guaranteed to be served within a maximum headway.
- **Optional stops** are only served when there is a request for transportation nearby.

Because the vehicle has freedom over which optional stops to serve and when, the resulting problem is a hard combinatorial optimization problem. Three complementary lines of work address it:

**Exact optimization.** A mixed-integer program with mandatory and optional clustered stops, accelerated by two techniques: separation of sub-tour elimination constraints, and a column generation reformulation. A pleasant property of the reformulation is that the restricted master yields *integer* optimal solutions, so branch-and-price is unnecessary. On 14 benchmark instances (up to 62,160 binary variables) column generation dominated both plain MIP and sub-tour separation from three buses upwards.

**Heuristics.** A destroy-and-repair large neighborhood search with randomized search and 2-opt on the routing part. It obtained solutions within an average gap of 1% or less of the optimum on all 14 benchmark instances within a second of runtime, and solved 22 larger instances typically in under a minute, occasionally orders of magnitude faster than the exact approach.

**Real-time operation.** A two-phase heuristic that re-optimizes as requests arrive: an insertion phase that re-routes when a new request shows up, and an improvement phase that re-optimizes the part of the plan that is not yet finalized. It achieved an average acceptance rate of 95.1% at an average gap of 6.5% with respect to the offline model.

A service-level comparison across demand levels showed the semi-flexible design improving service quality over a traditional feeder service by more than 60% (occasionally over 100%), at roughly 6% of the cost of a fully flexible on-demand service, while still serving passengers who do not pre-book.
