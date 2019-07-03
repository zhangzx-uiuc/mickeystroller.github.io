---
layout: post
title: Notes on a classic paper "A Sparse Sampling Algorithm for Near Optimal Planning in Large MDPs"
---

Why I write this note?
---
In Spring 2019, I took a seminar class [CS598: Statistical Reinforcement Learning](http://nanjiang.cs.illinois.edu/cs598/){:target="_blank"} given by [Prof. Nan Jiang](http://nanjiang.cs.illinois.edu/){:target="_blank"}. 
This class covers the theortical fundations of many topics in reinforcement learning such as planning, certainty-equivalence, state abstraction, fitted Q-iteration, exploration, and partial observability. 
I learned a lot in the class and really enjoyed it. 
In addition, this class includes a final project that requires us to either reproduce the proofs of an existing paper or conduct a novel research with *significant theoretical component*. 
Since I have no background on reinforcement learning theory, I decide to take the former type of project and reproduce the proofs of a classic paper in details. 

Why I choose this paper?
---
Probably the first thing I learned in the class is the difference between *learning* and *planning*. If the environment (or the model) is known, we do *planning*, otherwise, we do *learning*. This paper is particularly interesting as it studies a setting that we do have the environment information but **only through the access to a simulator**. As a result, we avoid the need to explicitly specifiy the huge environment. 

Talk is cheap. Show me the math. [<a href="\resources\CS598NJ\sparsesampling-journal.pdf" target="_blank">Original Paper</a>], [<a href="\resources\CS598NJ\report.pdf" target="_blank">My Note</a>], 
[<a href="\resources\CS598NJ\source.zip" target="_blank">LaTex Source</a>].

