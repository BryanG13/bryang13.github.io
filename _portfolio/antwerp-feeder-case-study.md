---
title: "Antwerp N177: a semi-flexible feeder service on a real corridor"
collection: portfolio
category: phd
permalink: /project/2023-antwerp-feeder-case-study
excerpt: "A case study that takes the semi-flexible feeder service out of the benchmark and into the real world, simulating a deployment along the N177 between Boom and central Antwerp against the existing De Lijn bus lines."
date: 2023-07-01
period: "2022 – 2023"
institution: "University of Antwerp (PhD, with De Lijn network data)"
role: "PhD researcher (first author)"
links:
  - label: "IFORS 2023 talk"
    url: "/talks/2023-ifors"
  - label: "Transportmetrica A (2023)"
    url: "https://doi.org/10.1080/23249935.2023.2227738"
---

The earlier work on the semi-flexible feeder service was tested on generated benchmark instances. This case study asks what happens on an actual corridor, using real road-network data and a real incumbent network as the benchmark.

The setting is the **N177 between Boom and central Antwerp**, a suburban corridor that is poorly served relative to its proximity to the city. The simulated service places **8 mandatory and 56 optional bus stops** along it, serves 100 passenger requests over a two-hour window, and guarantees a maximum headway of 20 minutes with a vehicle capacity of 20. Requests were generated on a realistic road network rather than assumed to be uniformly spread, and the results are compared against more than 20 existing De Lijn bus lines serving the same area.

The findings:

- **Service quality** improved by 31.6% on the global objective, and average user ride time dropped by 22% compared with the existing transit options.
- **Acceptance saturates at around 90%** once roughly 12 buses are available — beyond that, extra vehicles add little.
- There is a genuine trade-off in how much freedom the optimizer is given: with only 3 buses a near-perfect solution is achievable for accepted requests, but the global objective suffers. The sweet spot in the *degree of optimization freedom* is intermediate, not extreme — the same Goldilocks logic that runs through the service design itself.

The instance generation for this study was done with a custom generator built on OpenStreetMap road networks, so the demand and travel times reflect the actual corridor rather than an abstract network.
