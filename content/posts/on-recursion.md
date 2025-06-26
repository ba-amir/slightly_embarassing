---
title: "On Recursion"
date: 2025-06-02T14:11:22+01:00
draft: true
---

## Outline 

- introduction
- examples of recursive algorithms
- guidelines for writing recursive algorithms

## What is Recursion?

Recursion is a very simple thing to define. Unfortunately, the definition doesn't 
really get you anywhere if you don't already understand what recursion is. For this reason, 
I've decided it's best to just skip it for now. What we're going to do instead is outline 
a series of ideas that will hopefully give you a sketch for what recursion should look like. 
Once we're done with that sketch, the next section will fill in the details with more concrete
examples. We'll look at famous recursive algorithms, we'll compare them with iterative solutions, 
we'll take them apart to see how, and more importantly why, they work. And finally, in the last section, 

We're going to start our journey with recursive acronyms. That is, an acronym that refers to itself when 
expanded. As far as I can tell, the most common example is GNU which stands for GNU's not Unix. Take a minute to see how you 
long can expand this before your brain rebels against you. Luckily for you, your brain is actually capbable of rebelling, in 
other words you have agency. Imagine you were a mindless automaton given task of expanding acronyms, giving 
such an acronym you'd continue to expand and expand getting nowhere all the while until your batteries run out. 
What makes the recursive acronym so deadly to your average automaton is that they don't "bottom out". They 
don't have a way of indicating, "okay that's far enough. You may stop now". While this doesn't matter much 
for human conversation, in fact, one could say it is that promise of infinity that makes them interesting. 
Unfortunately for us, infinity tends to gum up the gears of computers. For now, we'll move on to somewhere else 
where infinity is usually more welcomed. 


Some functions in mathematics are defined in terms of themselves. A famous example is find the nth member of the 
Fibonacci sequence: 1, 1, 2, 3, 5, 8, 13 where every member is the sum of two previous numbers. The proper 
mathematical formulation is: 

F(1) = 1 
F(1) = 1 
F(n) = F(n - 1) + F(n - 2)



## Recursion Gallery

1. Addition
2. LinkedList
3. Binary Search
4. Merge Sort
5. 

## How do I do a Recursion
