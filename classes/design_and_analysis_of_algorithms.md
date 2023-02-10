---
layout: page
title: Design and Analysis of Algorithms
description: >
    "This is an intermediate algorithms course with an emphasis on teaching techniques for the design and analysis of efficient algorithms, emphasizing methods of application."
hide_description: false
sitemap: false
---

0. unordered list to be replaced by Hydejack Table Of Contents
{:toc}

## Overview

The class that made me good at LeetCode.
The class had three rough sections:
1. Greedy and Graph Algorithms
2. Linear Programming and Game Theory
3. Intractability

This page will mostly serve as a description of concepts taught.
Cheat sheet at the bottom also gives a great overview of all topics covered.

## Foundation

In order to analyze algorithms, you need tools.
Tools such as:
* Probability - Conditional, Expectation, Chernoff Bounds, Chebyshev's inequality, etc.
* Master Theorem - Can visualize an algorithm as a tree and use this to calculate asymptotic runtime.
* Amortized Analysis - Asymptotic runtime of a group of actions. Like how adding to a list is O(1)_a despite having to expand every *n* additions.
* Competitive Analysis - Prove that your online algorithm is, at worst, a constant multiple off the best offline algorithm.

### Hashing

Some amount of the class was spent rigorizing runtimes of hash-tables.
This necessitated knowledge of how to store the table and how to handle collisions.
As well as their respective effects on runtime.

## Greedy and Graph Algorithms

Honestly, there isn't much to say here.
This was mostly a skill building portion of the class.
First 2 PSets were dedicated towards building our intuition on how to think greedily.

## Linear Programming (LP)

Introduction into Weak/Strong LP duality.
This was mostly 

### Max Flow

Given a graph of "pipes" with a source and drain node, maximize flow to the drain.
We were proved Ford-Fulkerson and Edmonds-Karp algorithms to use later in class.

### Game Theory

Give an elaborate game of *rock, paper, scissors*, find the best strategy.
We were provided tools in which to find Nash Equilibriums in 2-player, 0-sum games.
Also covered Gedanken Experiments for randomized games.

## Intractability

The class introduced the P vs NP problem and how to do reductions.
There's also plenty of induction in the class.

Given that we weren't going to solve all of these problems in class, we also covered approximation algorithms that are guaranteed to within some constant multiple of the best solution.

Honestly, page 3 of my cheat sheet provides the most comprehensive view of the material.

I also took the class [Automata, Computability, and Complexity Theory](automata_computability_and_complexity.md) which goes into greater depth in this field.

## My Cheat Sheet

Above sections are very broad strokes but if you want 99% of everything covered in that class, here is my cheat sheet.

{% pdf "/assets/pdf/6_046_Cheat_Sheet.pdf" %}

