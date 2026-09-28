---
title: "Parameter Space Search: a metaheuristic that searches the parameters of a constructive heuristic"
collection: portfolio
category: phd
permalink: /project/2023-parameter-space-search
excerpt: "A new type of metaheuristic framework, developed during my PhD, in which an outer simulated annealing searches the parameter space of an inner semi-random greedy constructive heuristic — instead of searching the solution space directly."
date: 2023-09-01
period: "2021 – 2023"
institution: "University of Antwerp (PhD, joint with KU Leuven)"
role: "PhD researcher (first author)"
links:
  - label: "Networks (2023)"
    url: "https://doi.org/10.1002/net.22185"
  - label: "CLAIO 2022 talk"
    url: "/talks/2022-claio"
---

Most metaheuristics perturb or recombine *solutions*. Parameter Space Search (PSS) perturbs *parameters* instead. A semi-random greedy constructive heuristic is run repeatedly under randomized construction parameters — including a feasibility ratio and a pilot method — and an outer simulated annealing searches that parameter space.

The motivation is diversity. Because consecutive runs behave quite differently, the framework explores far more of the feasible region than a single restarting heuristic, which is what makes it able to find feasible solutions on strictly constrained instances where other metaheuristics stall. It is also agnostic to the problem: the same outer search can be applied to a different inner constructive heuristic without redesigning the framework.

On 42 benchmark instances (2 to 12+ buses, up to 90 requests and 19 to 55 stops with a 20-minute maximum headway) the framework performed on average **12.42% better than LocalSolver**, a commercial optimization solver given a full one-hour budget on 12 threads, with an average runtime of 2.1 seconds and up to 21% better on individual instances. Larger instances were solved typically within 2 minutes. Parallelising the repeated inner runs gave a speedup of 2.6× on average and 5.11× at best.

The framework is described in my paper *A demand-responsive feeder service with a maximum headway at mandatory stops* (Networks, 2023).
