---
title: "Jain–Sah–Sawhney: Singularity of discrete random matrices"
layout: blogpost
description: The singularity probability for discrete random matrices.
---

[Vishesh Jain](https://math.mit.edu/~visheshj/), [Ashwin Sah](http://www.mit.edu/~asah/), and [Mehtaab Sawhney](http://www.mit.edu/~msawhney/) just posted two amazing papers: *Singularity of discrete random matrices* [Part I](https://arxiv.org/abs/2010.06553) and [Part II](https://arxiv.org/abs/2010.06554).

<figure>
  <img src="/blog/images/vishesh-jain-2020.jpg" width = "153">

  <img src="/blog/images/ashwin-sah-2020.jpg" width = "133">
  
  <img src="/blog/images/mehtaab-sawhney-2020.jpg" width = "160">
  
  <figcaption>Vishesh Jain, Ashwin Sah, and Mehtaab Sawhney</figcaption>
</figure>

**The singularity problem for random matrices:** what is the probability that a random $n\times n$ matrix with independent 0/1 entries is singular?

The first non-trivial bound on this problem was by Komlós in 1967. After a long series of works by many mathematicians including Kahn, Komlós, Szemerédi, Tao, Vu, Bourgain, Wood, Rudelson, and Vershynin, a breakthrough was recently achieved by [Tikhomirov](https://annals.math.princeton.edu/2020/191-2/p06), who showed that, when the matrix entries are iid uniform from $$\{0,1\}$$, the probability of singularity if $(1/2 + o(1))^n$, which is tight since with probability $2^{-n}$ the first row is zero.

The new papers of Jain–Sah–Sawhney consider a natural extension of the singularity problem where each entry of the $n\times n$ matrix is iid: 1 with probability $p$ and 0 with probability $1-p$, for some value of $p$ other than 1/2.

A folklore conjecture in this area states that the main reason for the singularity of such random matrices is the presence of two equal rows/columns or some zero row/column:

**Conjecture.** For a fixed $0 < p < 1$, the probability that a random $n\times n$ matrix with iid Bernoulli(_p_) entries is singular is $1+o(1)$ times the probability that the matrix has one of the following: (a) two equal rows, (b) two equal columns, (c) a zero row, (d) a zero column.

Note that even Tikhomirov's breakthrough result does not give precise enough results to answer this conjecture. However, we now have the following incredible result.

**Theorem.** (Jain–Sah–Sawhney) The above conjecture is true for all $p \ne 1/2$.

(The case $p = 1/2$ remains open.)

In fact, they prove something much more general: namely that the above result remains true if the random matrix entries are iid discrete random variables that are _non-uniform on its support_. Furthermore, they prove nearly tight bounds on the probability of these matrices having small least singular values. Very impressive!