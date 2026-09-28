---
title: "Assigning students to schools under capacity and priority rules"
collection: portfolio
category: phd
permalink: /project/2022-school-assignment
excerpt: "A school choice assignment problem for a real district: place 8,500 students across 86 schools within capacity while honouring ranked preferences, a protected share of places for priority students, and the rule that children with relatives at a school get preference there."
date: 2022-02-01
period: "2022"
institution: "University of Antwerp (side project during the PhD)"
role: "PhD researcher"
---

Every year a school district has to do something that looks like a matching problem and behaves like a negotiation. Students submit a ranked list of schools, every school has a hard capacity, and a handful of rules sit on top that are not negotiable at all: a reserved share of places for priority students, and preference for children who have relatives already at a particular school. Get the mechanism wrong and the district is the one paying for it.

**The data.** The real instance came from a single district and was provided by a collaborator, with **8,500 students** across **86 schools**. Each student has a ranked list of preferred schools, a priority flag, and a list of schools where they have relatives. Each school has a total capacity and the percentage of it reserved for priority students. Alongside it I built synthetic scenarios of **75 schools and 6,000 to 8,000 students** across five capacity settings, so the mechanisms could be compared on size rather than on one particular district's politics.

**Two mechanisms, side by side.** The point of the project was to compare mechanisms rather than to build one clever algorithm, so I implemented two in C++.

The first is a randomized constructive assignment. Each school holds a ticket list, and when a place opens the algorithm reaches into that list. Two adjustments decide who is at the front: students with relatives at that school are moved up, and when a school is working through its reserved capacity the priority students are moved up instead. The second is **serial dictatorship**, the mechanism design classic, where students are served in a random order and each simply takes the best school that still has room.

**Isolating the rules.** The interesting part was not either mechanism on its own but what each rule is worth. The real instance was therefore run in four variants, crossing the priority rule on and off against the relatives rule on and off. That is what turns a policy argument into something you can put a number on, and it is the part I would want a district to look at before deciding which rule to keep.

*The comparison was run and the results workbook exists, but it is not part of the current archive, so this entry describes the problem and the mechanisms rather than reporting the measured trade-offs. The data provider is not named here without permission.*
