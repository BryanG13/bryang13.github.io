---
title: "School bus routing for students with special needs"
collection: portfolio
category: industry
permalink: /project/2022-school-bus-routing
excerpt: "A capacitated school bus routing problem with accessibility constraints, solved on real De Lijn data for the municipalities of Diest and Gavere. A good illustration of how a hard routing problem looks once mobility constraints are added."
date: 2022-06-01
period: "2022"
institution: "De Lijn (Flemish public transport operator)"
role: "Optimization consultant, side project during the PhD"
---

Not every school journey is a school journey. Transporting students with special needs means the vehicle capacity is constrained by more than headcount: wheelchairs and mobility aids occupy space, individual students have to be picked up at their own address, and the round trip has to fit school start and end times without waiting hours on the kerb.

This project built and solved that capacitated school bus routing problem for the municipalities of **Diest** and **Gavere**, using real De Lijn data: actual address lists, actual travel-time matrices, earliest and latest arrival times, and per-student **wheelchair requirements**, over fleets of 18 vehicles in Diest and 9 in Gavere. Travel times were supplied as minimum, average and maximum variants, which is a more honest input than a single average would have been. The solution work was a large neighborhood search and a local search implementation in C++, with a Python layer on top for instance handling and visualization.

Working from real data rather than synthetic instances made the modelling trade-offs visible in a way benchmark data never does: which constraint actually binds, and which assumptions quietly drive the objective value.
