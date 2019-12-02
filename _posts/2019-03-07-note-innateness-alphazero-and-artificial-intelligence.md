---
title: "notes on paper \"Innateness, AlphaZero, and Artificial Intelligence\""
date: 2019-03-07
categories: code

classes:
  - wide
---

This is the probably the most convincing paper I have read on arguing the power of the current state-of-art artificial intelligence, namely the AlphaGo Series (AlphaGo, AlphaGo Zero, AlphaZero). While the DeepMind said that it's the most challenging of domains and it needs no knowledge of the domain beyond basic rules, Gary Marcus, author of this paper, questions this statement, and believes that artificial intelligence needs greater attention to innateness, which is the main subject of this paper.

Click [here](https://arxiv.org/ftp/arxiv/papers/1801/1801.05667.pdf) to read the original paper.

I will only list my key notes on the paper since this paper does not have a conclusion.

## key notes
- there is an old debate on how much of the human mind is built-in, and how much of it is constructed by experience. Humans are born with significant amounts of innate machinery, mainly from biological inheritance, for example, neonates can distinguish speech from closely-matched sine-wave analogues. The guiding question of this paper is whether artificial intelligence ought to go the same way, or they can learn in a *tabula rasa* fashion;
- `cognition = f(a, r, k, e)`, where:
    - *a* = innate algorithms (whether domain-specific or domain-general)
    - *r* = innate representational formats (domain-specific or otherwise)
    - *k* = innate knowledge (domain-specific or otherwise)
    - *e* = experience
- a true blank slate would set *k* and *r* to zero, set *a* to some extremely minimal value, and leave the rest to experience. While the DeepMind claimed it mastered the game of Go without human knowledge, which basically means a "blank slate", most of the reinforcement learning paper's seventeen authors were deeply familiar with Go, and DeppMind used innately built-in Monte Carlo search tree besides reinforcement learning, which contributed to both *a* and *r* not being zero. The convolutional layers were also not purely learned by reinforcement learning, as well as a special sampling algorithm dealing with symmetries. All of these approaches were not *tabula rasa*, against the claim that made about AlphaGo;
- early implementation of hacking the Atari game was more *tabula rasa*. As DeepMind added more and more innateness to later architectures, they became more powerful;
- with the right initial algorithms and knowledge, complex problems are learnable. Without the right initial algorithms, representations and knowledge, many problems remain out of reach;
- the game of Go is a game with perfect information. It is not the most challenging of domains as it was claimed. For example, the transportation optimization;
- a preliminary list by Gary Marcus on the subjects that might be helpful to support artificial general intelligence:
    - representations of objects
    - structured, algebraic representations
    - operations over variables
    - a type-token distinction
    - a capacity to represent sets, locations, paths, trajectories, obstacles and enduring individuals
    - a way of representing the affordances of objects
    - spatiotemporal contiguity
    - causality
    - translational invariance
    - capacity for cost-benefit analysis
    - and, *representation of time*
- the important point, for present purposes, is, that there is a whole world of possible innate mechanisms that AI researchers might profitably consider; simply presuming by default it is desirable to include little or no innate machinery seems, at best, close-minded. And, at worst, an unthinking commitment to relearning everything from scratch may be downright foolish, effectively putting each individual AI system in the position of having to recapitulate a large portion of a bilions years of evolution;
- it's time for AI to take nativism more seriously.