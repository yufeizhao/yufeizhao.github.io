---
title: "Upper tails for random regular graphs"
layout: blog
description: Ben Gunby's new paper determining the large deviation rate for sparse random regular graphs.
draft: true
---

[Ben Gunby](https://sites.google.com/view/benjamingunby/home), a final-year PhD student at Harvard whom I advise, just posted his paper [_Upper tails of subgraph counts in sparse regular graphs_](https://arxiv.org/abs/2010.00658). This is a substantial paper that unveils surprising new phenomena for the problem of large deviations in random graphs.

{% include blog_image
    src = "ben-gunby-2020.jpg"
    width = "300"
    caption = "<a href=\"https://sites.google.com/view/benjamingunby/home\">Ben Gunby</a>"
%}

**Problem.** What is the probability that a random graph has far more copies of some given subgraph than expected?

This is called the "upper tail" problem for random graphs.
It is a problem of central interest in probabilistic combinatorics.
There was a lot of work on this problem for the classic Erdős–Rényi random graph $G(n,p)$ (with edges appearing independently at random), with a lot of exciting recent developments.
Ben considers the upper tail problem for _random regular graphs_, another natural random graph model. 
Random regular graphs are usually harder to analyze since the random edge appearance are no longer independent, and this increased difficulty also shows up for the upper tail problem.

Let me highlight one specific result in Ben's paper (Theorem 2.9).

**Theorem.** ([Gunby](https://arxiv.org/abs/2010.00658)) _Let $$G_n^d$$ be a random $d$-regular graph, where $d = d(n)$ depends on $n$. Assume that $dn$ is even and and $$n^{14/15}\log n \le d = o(n)$$. Let $X$ denote the number of copies of_ 
  <img src="/blog/images/k24plusedge.svg" width="80" />
_in $$G_n^d$$. Then for every fixed $$\delta > 0$$ (here $$\sim$$ means up to $1+o(1)$ factor),_

$$
-\log \mathrm{Pr}(X \ge (1+\delta)\mathbb{E} X) \sim  \frac{(18\delta)^{1/3}}{2} \frac{d^3}{n} \left(\log \frac{n}{d}\right)^{2/3} \left(\log\log \frac{n}{d}\right)^{1/3}
$$

<br />

This result is surprising. 
The appearance of the second loglog term has not been observed in previous works on the upper tail problem. 
It is even more impressive that Ben was able to prove such a sharp estimate.

Understanding these large deviation probabilities roughly corresponds to understanding the "dominant reason" for rare events. Roughly speaking, the above loglog term appears because the dominant reason **is not the presence of some fixed subgraph (e.g., a large clique or hub), unlike all earlier results.** 
Something else more subtle is happening.
While we still do not understand the complete picture, Ben's result provides strong evidence why the upper tail problem for random regular graphs may be substantially more intricate than that of $G(n,p)$.

In this blog post, I will tell you some history and background of the upper tail problem in random graphs.
I will try to explain why Ben's result is surprising. 
Lastly, I will also mention a recent paper I have with Yang Liu on the [upper tail problem in random hypergraphs](https://arxiv.org/abs/1910.02916), where a different new phenomenon is observed.


## Chasing the infamous upper tail

Roughly, and intuitively, to gain a precise understanding of the upper tail problem, we are really asking:

> _What are the dominant reasons for the rare event that a random graph $G(n,p)$ has way too many triangles?_

We can now say confidently the following:

> _It is primarily because the such a rare random graph contains roughly a large clique or a large hub._

Here a "hub" is a set of vertices adjacent to all other vertices.
It is not hard to see that planting a large clique or hub in a $G(n,p)$ would automatically generate many additional triangles (these triangles may use also the edges of the random graph).

For example, the following theorem
is the culmination of a long line of work by many researchers.

(We use the following asymptotic notation, which is standard in this line of work: $$f \ll g$$ means $f = o(g)$.)

**Theorem.** _Let $X$ denote the number of triangles in $G(n,p)$. Then, for $n^{-1/2} \ll p \ll 1$ and fixed $\delta > 0$, one has_

$$
-\log \mathrm{Pr}(X \ge (1+\delta) \mathbb{E} X)
\sim \min \left\{\frac{\delta}{3}, \frac{\delta^{2/3}}{2}\right\} n^2p^2\log\frac{1}{p}
$$

The problem of estimating the upper tail $\mathrm{Pr}(X \ge (1+\delta) \mathbb{E})$ has a long history.
Janson and Rucinski called this problem the [infamous upper tail](http://www2.math.uu.se/~svante/papers/sj137.pdf), which had resisted a wide range of techniques that researchers have used to tackle this problem.
This upper tail problem was an excellent litmus test in the development of concentration inequalities.


{% include blog_image
    src = "infamous-upper-tail.svg"
    width = "400"
%}

Several significant breakthroughs then occurred on this problem over the past decade.

[DeMarco–Kahn](https://arxiv.org/abs/1005.4471) and [Chatterjee](https://arxiv.org/abs/1003.3498) independently determined the order of magnitude of the log-probability in the above upper tail problem, for triangle counts in a random graph.
Their work closed a log-factor gap left by previous methods developed by [Kim–Vu](https://doi.org/10.1002/rsa.10113).

The next goal was then to pinpoint the tail probability. This led to further developments of powerful tools.

The seminal work of [Chatterjee and Varadhan](https://arxiv.org/abs/1008.1946) developed a **large deviation principle** for the upper tail problem in random graphs, thereby reducing the problem to a **variational problem** in the space of graphons, i.e., graph limits. Their work paved the way for much further development, which has two complementary strands:

**1. Extending the large deviation framework to sparser graphs.** Chatterjee and Varadhan's proof uses Szemerédi's graph regularity lemma, which only allows us to handle dense graphs (here for random graphs $G(n,p)$ _dense_ means constant $p$, whereas _sparse_ means $p = o(1)$). Further work, starting with [Chatterjee–Dembo](https://arxiv.org/abs/1401.3495)'s "non-linear large deviations", as well as further improvements by [Eldan](https://arxiv.org/abs/1612.04346), [Cook–Dembo](https://arxiv.org/abs/1809.11148), [Augeri](https://arxiv.org/abs/1810.01558), [Harel–Mousset–Samotij](https://arxiv.org/abs/1904.08212), and [Basak–Basu](https://arxiv.org/abs/1912.11410), allow us to handle much sparser densities of graphs.

For certain subgraphs, including cliques, we now have a very precise understanding thanks to [Harel–Mousset–Samotij](https://arxiv.org/abs/1904.08212), who gave a short and clever [container](https://arxiv.org/abs/1801.04584)-inspired combinatorial argument in the case of triangles.

**2. Solving the variational problem.** The above large deviation frameworks reduces the problem of estimating the tail probability to another problem---a variational problem in the space of graphons. 

_Variational problem for upper tails:_ Among edge-weighted graphs with some prescribed subgraph density, determine the minimum possible relative entropy (a certain non-linear function of the edge-weights)

These variational problems are more difficult than classical problems in extremal graph theory. In fact, despite [some progress](https://arxiv.org/abs/1210.7013), we still do not understand how to solve such problems exactly in the "dense" regime.


For sparse graphs $G(n,p)$ with $p \to 0$, the variational problem was solved asymptotically in the case of clique subgraphs by [Lubetzky–Zhao](https://arxiv.org/abs/1402.6011), and for more general subgraph counts by [Bhattacharya–Ganguly–Lubetzky–Zhao](https://arxiv.org/abs/1507.04074).


Putting the two complementary pieces together allow us to pinpoint upper tail probabilities. Similar to the case of triangles, the main message is, roughly speaking,

> _The dominant reason for a random graph to have too many copies of some fixed $H$ is that it contains a large clique or a large hub._

**Theorem.** _Let $H$ be a graph with maximum degree $$\Delta$$. Let $\delta > 0$.
Let $X$ be the number of copies of $H$ in $G(n,p)$. Provided that $n^{-\alpha_H} \le p = o(1)$ (where $\alpha_H$ is some explicit constant that has improved over time),
one has_

$$
-\log \mathrm{Pr} (X \ge (1+\delta)\mathbb{E} X) \sim c(H, \delta) p^{\Delta} n^2 \log \frac{1}{p},
$$

_where $$c(H,\delta) > 0$$ is an explicit constant determined in [Bhattacharya–Ganguly–Lubetzky–Zhao](https://arxiv.org/abs/1507.04074)._

While this is a pretty satisfactory formula, our understanding is still not complete.

1. Is the result valid for the "full" range of $p$?

2. What precise statements can you make about the conditioned random graph? (see [Harel–Mousset–Samotij](https://arxiv.org/abs/1904.08212))

## Gunby's work on random regular graphs

Ben Gunby's work studies the upper tail problem for random regular graphs:

**Problem.** Let $X$ be the number of copies of some given subgraph $H$ in a random $d$-regular graph $G_n^d$. Estimate $-\log \mathrm{Pr}(X \ge (1+\delta)\mathbb{E} X)$, when $$n^{1-c} \le d = o(n)$$.

There is a similar dichotomy of steps as above: 

1. Proving a large deviations framework, which, for the most part, can be deduced directly from the $G(n,p)$ version, though there are some annoying technicalities (the "tilting" argument for lower bounding probabilities  requires further arguments).

2. Solving the variational problem -- this is where new difficulties and innovations lie.

A recent paper of [Bhattacharya–Dembo](https://arxiv.org/abs/1909.03045) (this is by Sohom Bhattacharya and not my coauthor [Bhaswar Bhattacharya](http://www-stat.wharton.upenn.edu/~bhaswar/) mentioned earlier) essentially solved the variational problem when $H$ is a regular graph (Ben had also independently worked out the case when $H$ is a cycle).

Ben Gunby's new paper solves the variational problem for "most" graphs $H$ (those that satisfy some technical condition), which includes all graph $H$ with average degree greater than 4, as well as pretty much all small graphs. 

For most graphs $H$, the upper tail has "expected" behavior, meaning that the dominant reason for seeing many copies of $H$ is, very roughly speaking, the presence of some large planted subgraph. The resulting tail probability formulas also resemble what we have seen earlier:

$$
-\log \mathrm{Pr}(X \ge (1+\delta) \mathbb{E} X) \sim \rho(H, \delta) n^2 (d/n)^{2+\gamma(H)} \log(n/d).
$$

for some graph parameter $$\gamma(H)$$, whose role here is far from obvious.

For every graph $H$, Ben manages to bound the log-probablity within a log-factor gap:

$$
n^2 (d/n)^{2+\gamma(H)} \lesssim -\log \mathrm{Pr}(X \ge (1+\delta) \mathbb{E} X) \lesssim n^2 (d/n)^{2+\gamma(H)} \log(n/d)
$$

The most surprising part of Ben's paper is that for some $H$, the upper tail is not "expected" as above, i.e., the asymptotic formula two display equations earlier is incorrect for this $H$. 

For the graph <img src="/blog/images/k24plusedge.svg" width="60" />, Ben solves the variational problem, which led to the formula at the beginning of this post. The  solution turns out to come not from "planting a subgraph" but rather from some other more delicate construction.

It remains to be seen what happens to other graphs $H$. 
Will we need even more intricate constructions?
What does this mean for techniques towards solving the upper tail problem for the full range of degree parameters? There is still lot that we do not understand.

## Large deviations for random hypergraphs

In a recent paper with [Yang Liu](https://arxiv.org/abs/1910.02916) (to appear in _Random Structures & Algorithms_), we considered the extension of the upper tail problem to random hypergraphs. 
Yang Liu is a PhD student at Stanford. We started this work while Yang was an undergraduate student at MIT.

{% include blog_image
    src = "yang-liu-2020.jpg"
    width = "200"
    caption = "<a href=\"https://yangpliu.github.io/\">Yang Liu</a>"
%}

Consider the random $k$-uniform hypergraph $$G^{(k)}(n,p)$$, where every unordered $k$-tuple of vertices appears as an edge independently with probability $p$.

**Problem.** Given a $k$-uniform hypergraph $H$. Let $X$ denote the number of copies of $X$ in $$G^{(k)}(n,p)$$. Estimate $\mathrm{Pr}(X \ge (1+\delta)\mathbb{E} X)$.

As before, there are two complementary strands (1) developing large deviation framework and (2) solving the variational problem. 
Some of the work towards (1) for random graphs can be transferred over to the hypergraph setting. Towards (2), we solve the variational problem asymptotically for some $H$, and make a conjecture for what we believe should happen for general $H$. 

We show that one cannot naively extend the upper tail results from random graphs to random hypergraphs.
In our paper, we take the readers on a long discussion through several iterations of naive conjectures and counterexamples, eventually building up to our final conjecture, which takes some effort to state, but very roughly, says that

> _The dominant reason for upper tails in random hypergraphs is the presence of a collection of "stable mixed hubs."_

For both random regular graphs and random hypergraphs, these recent results highlight unexpected phenomena.
They illustrate the richness of the problem and lead us to more questions than answers.