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

The brief also left the harder questions open on purpose, and it is worth recording that they were open: how to handle breaks, whether patrols have to return to their starting point, how to treat interruptions, and what the genuinely dynamic version of the problem looks like. In this project, I covered the modelling of the problem. 
