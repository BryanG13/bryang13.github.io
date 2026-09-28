---
title: "Optimizing police patrol routes for unpredictability"
collection: portfolio
category: industry
permalink: /project/2020-police-patrol-routing
excerpt: "Planning daily routes for the mobile unit of the Belgian police, where the objective is not just to cover the beat but to keep the route unpredictable, so that patterns cannot be learned and exploited."
date: 2020-06-01
period: "2020"
institution: "Belgian police, mobile unit"
role: "Optimization consultant"
---

The mobile unit spends its whole shift driving between patrol locations, which makes it the part of the police force where routing is a genuine planning problem. The brief I worked from was specific about the difficulty. Every patrol location has a **priority level from 0 to 5**, an **expected visit duration** that ranges from a few seconds to an hour, and often a **time window** for arrival. Recurrent locations must be visited repeatedly within a shift, with a minimum time between two visits and a maximum, the maximum existing specifically to stop all twelve of a location's visits being crammed into the first eight hours and none into the last four. The travel time matrix came from Google Maps and is time dependent.

**Visits, not locations.** The modelling decision that made this tractable was to stop treating a patrol location as a single node. Instead, every location generates as many **visits** as it needs to be visited, and each visit is either mandatory or optional. A location needing twelve visits might have eight mandatory and four optional. Each optional visit then carries a score derived from the location's priority and from how often the location must be visited, so the first optional visit of a busy location can score higher than the second. The objective is to maximize the total score of the optional visits actually performed, which is the same as minimizing the score left unperformed.

**Making the route unpredictable.** This was the part that made the project worth doing. The idea is to forbid **patterns**, where a pattern is a sequence of consecutive patrol locations. A pattern may occur at most once, or at most some small number of times. A route of nine locations under a pattern length of three yields the patterns ABA, BAC, ACD, CDB, DBA and BAE, none of which may repeat. Three parameters then set how strongly unpredictability is enforced: the pattern length (at least 2), the number of times a pattern may occur (at least 1), and how far back in the past to look when collecting patterns that already happened (a couple of hours, or three days). The practical consequence is that the schedule cannot be a single daily plan produced once. It has to be interrupted and re-optimized, and the forbidden pattern list is rebuilt on every pass.

**Algorithm.** A constructive heuristic, running several construction methods in parallel, with as much forward scheduling as possible and **no local search at all**. The brief gave two reasons: time dependent travel times make local search hard, and the schedule gets interrupted and re-optimized often enough that a construction that is easy to resume is worth more than a neighbourhood that would search better. For each unit the candidate patrols are built, sorted by score, and the algorithm repeatedly picks at random from the best G of them, updating both the patrol list and the forbidden pattern list, keeping the solution with the lowest total weight of unperformed patrols at the end. Candidates are pruned along the way, dropping any patrol to the same location that has lower weight than a mandatory one, any that is too far away, any that would create a forbidden pattern, and any that cannot be reached and returned from before the end of the shift. A set of forbidden intervals prevents two different units from visiting the same location inside the minimum inter-visit time.

The brief also left the harder questions open on purpose, and it is worth recording that they were open: how to handle breaks, whether patrols have to return to their starting point, how to treat interruptions, and what the genuinely dynamic version of the problem looks like.

*This project covered the model and the proposed algorithm. The archive contains the formulation and the algorithm proposal, but no documented implementation or results, so this entry describes the design rather than reporting measured performance.*
