---
title: "Kwan–Sah–Sawhney–Simkin: High-girth Steiner triple systems"
layout: blogpost
image: /blog/kwan-sah-sawhney-simkin-2022.jpg
description: Resolution of a 1973 Erdős conjecture showing the existence of Steiner triple systems with arbitrarily high girth.
twitter_large_image: true
---

There is an impressive new preprint titled [High-Girth Steiner Triple Systems](https://arxiv.org/abs/2201.04554) by Matthew Kwan, Ashwin Sah, Mehtaab Sawhney, and Michael Simkin.
They prove a 1973 Erdős conjecture showing the existence of Steiner triple systems with arbitrarily high girth.

{% include blog_image
    src = "kwan-sah-sawhney-simkin-2022.jpg"
    width = "600"
    caption = "Matthew Kwan &nbsp;&nbsp;&nbsp; Ashwin Sah &nbsp;&nbsp;&nbsp; Mehtaab Sawhney &nbsp;&nbsp;&nbsp; Michael Simkin"
%}

An order _n_ **triple system** is defined to be a set of unordered triples of $\{1, \dots, n\}$. 
Furthermore, it is a **Steiner triple system** if every pair of vertices is contained in exactly one triple.

An example of a Steiner triple system is the Fano plane, illustrated below.

{% include blog_image
    src = "fano-plane-numbered.svg"
    width = "300"
%}

Here each line or circle represents a triple containing its elements. Note that every pair of vertices lies in exactly one line/circle (this is what makes it Steiner).

<!-- We can explicitly list the triples as follows:

```
123
1  45
1    67
 2 4 6
 2  5 7
  34  7
  3 56
``` -->

Steiner triple systems are old and fascinating objects that occupy a central place in combinatorics. For example, see this [Quanta Magazine article](https://www.quantamagazine.org/150-year-old-math-design-problem-solved-20150609/) for a popular account on Steiner triple systems and recent breakthroughs in design theory.

In the past decade, since Peter Keevash's [2014 breakthrough](https://arxiv.org/abs/1401.3665) proving the existence of designs, there has been a flurry of exciting developments by many researchers settling longstanding open problems related to designs and packings. Several related results were also featured in Quanta magazine:
[Ringel’s conjecture](https://www.quantamagazine.org/mathematicians-prove-ringels-graph-theory-conjecture-20200219/),
[Erdős–Faber–Lovász conjecture](https://www.quantamagazine.org/mathematicians-settle-erdos-coloring-conjecture-20210405/),
[_n_-queens problem](https://www.quantamagazine.org/mathematician-answers-chess-problem-about-attacking-queens-20210921/).

The new work proves the existence of Steiner triple systems with a desirable additional property: high girth.

In a graph, the *girth* is defined to be the length of a shortest cycle. The girth of a triple system is defined as follows (see the first page of the paper for some [motivation](https://arxiv.org/pdf/2201.04554.pdf) behind this definition).

**Definition.** The **girth** of a triple system is the smallest positive integer *g* so that there exist *g* triples occupying no more than $g+2$ vertices. (If no such *g* exists, then we say that the girth is infinite.)

Here is the main result of the new paper, which settles the Erdős conjecture.

**Theorem** ([Kwan—Sah—Sawhney–Simkin](https://arxiv.org/abs/2201.04554)). For all sufficiently large $n \equiv 1,3 \pmod{6}$, there exists a Stein triple system whose girth tends to infinity as $n \to \infty$.

They build on previous works by
[Glock, Kühn, Lo, and Osthus](https://arxiv.org/abs/1802.04227)
and
[Bohman and Warnke](https://arxiv.org/abs/1808.01065)
proving the existence of "approximate" Steiner triple systems (meaning having $1-o(1)$ fraction of the maximum possible number of triples).

Before this work, it was not even known if there existed infinitely many Stein triple systems with girth ≥ 10.

The proof uses a stunning array of techniques at the frontier  of extremal and probabilistic combinatorics, including recently developed tools for random greedy algorithms, as well as the iterative absorption method.