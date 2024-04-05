---
title: "Algorithms and Datastructures Project"
excerpt: "This is our (made together with Yves van Haaren) solution to the Pumps problem posed in the course Algorithms and Datastructures at Radboud University. Grade: 9.6 <br/><img src='/images/500x300.png'>"
collection: portfolio
---

The problem in short
----
The problem concerns the flooding of the Dutch *polders*. There is a provided graph where some notes are marked as containing a pumping station. Each edge has a different cost to traverse. When you are at a node with a pump you may turn it on to start pumping out water at a constant flow. The problem in short is given a certain starting location how can you traverse the graph such that you pump as much water out of the polders in total given a certain time frame.

Key parts of our solution
----
1. We first reduced the graph to only contain nodes marked as having a pump. This was done using Dijkstra's algorithm. 

2. For the second part we utilised dynamic programming. We reduced the problem to minimizing the sum of the commencement times of the pumps. We have developed a rather extensive recurrence relation for this part of the solution, which is further specified and mathematically supported (not a formal proof) in our report included in the git repository.
