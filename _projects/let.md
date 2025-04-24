---
layout: project
title: "Directed Acyclic Graph to Optimal Logical Execution Time"
subtitle: "Turning a DAG into an Optimal LET Schedule table"
usemathjax: true
---

This project is about converting a given Directed Acyclic Graph (DAG) to an optimal Logical Execution Time (LET) design. We can think of LET design as a schedule table with logical deadlines for each task, rathan than the actual physical deadline. The optimality aspect ensured that vertical core parallelisms is maximized, and horizontal length is minimzed, given a **timing** and **core** constraints. Everything was implemented through the help of Constraint Programming using Z3 in Python. Below are three illustrative charts:

We take this DAG as input, and two constraints: number of cores **k**, and timing constraint **t_const**. Let's assume for our application **min_cores = 2**.

<p align="center">
  <img src="/assets/projects/dag.png" alt="Pipeline" width="800" height="600">
</p>

**Example 1**: We specify that we have **k = 2** cores available on our multicore platform and **t_const = 8000ms**. We get this corresponding Optimal LET schedule table:

<p align="center">
  <img src="/assets/projects/k2.png" alt="Pipeline" width="750" height="600">
</p>


**Example 2**: We specify that we have **k = 3** cores available on our multicore platform and **t_const = 8000ms**. We get this corresponding Optimal LET schedule table (*It only took **6000ms**, since we have more resources!*):

<p align="center">
  <img src="/assets/projects/k3.png" alt="Pipeline" width="750" height="600">
</p>

The solution is generalizable for any $$k \in \mathbb{N}$$
