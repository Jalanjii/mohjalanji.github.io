---
layout: project
title: "Directed Acyclic Graph to Optimal Logical Execution Time"
subtitle: "Turning a DAG into an Optimal LET Schedule table"
---

This project is about converting a given Directed Acyclic Graph to an optimal Logical Execution Time (LET) design. We can think of LET design as a schedule table with logical deadlines for each task, rathan than the actual physical deadline. The optimality aspect ensured that vertical core parallelisms is maximized, and horizontal length is minimzed, given a **timing** and **core** constraints. Everything was implemented using Constraint Programming using Z3 in Python language. Below are some illustrative charts.

