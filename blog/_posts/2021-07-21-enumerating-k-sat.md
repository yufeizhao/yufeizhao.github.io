---
title: "Enumerating k-SAT functions"
layout: blogpost
image: /blog/images/nitya-dingding-2021.jpg
description: How many <i>k</i>-SAT functions are there? What does a typical one look like?
twitter_large_image: true
---

{% include blog_image
    src = "nitya-dingding-2021.jpg"
    width = "400"
    caption = "Nitya Mani and Dingding Dong"
%}

In a new paper coauthored with graduate students [Dingding Dong](https://www.math.harvard.edu/people/dong-dingding/) and [Nitya Mani](http://math.mit.edu/directory/profile.php?pid=2315) titled [_Enumerating k-SAT functions_](https://arxiv.org/abs/2107.09233), we study these fundamental questions about _k_-SAT functions:

- How many _k_-SAT functions on _n_ boolean variables are there? 
- What does a typical such function look like?

These questions about _k_-SAT functions were first studied by [Bollobás, Brightwell, and Leader (2003)](https://mathscinet.ams.org/mathscinet-getitem?mr=1968421), who made the following conjecture.

**Conjecture.** Fix $k \ge 2$. Almost all _k_-SAT functions are unate.

Here an [_unate function_](https://en.wikipedia.org/wiki/Unate_function) is a _k_-SAT function is one that can be turned monotone by first negating some subset of variables.

More precisely, the conjecture says that, as $n \to \infty$, $1-o(1)$ fraction of all _k_-SAT functions on _n_ boolean variables are unate.

An easy argument shows that there are $(1+o(1))2^{\binom{n}{k} + n}$ unate functions. So the above conjecture can be equivalently restated as:

**Conjecture.** Fix $k \ge 2$. The number of _k_-SAT functions on n boolean variables is $(1+o(1))2^{\binom{n}{k} + n}$.

The conjecture was previously proved for $k=2$ ([Allen 2007](https://mathscinet.ams.org/mathscinet-getitem?mr=2350165)) and $k=3$ ([Ilinca and Kahn 2012](https://mathscinet.ams.org/mathscinet-getitem?mr=3009746)) using the (hyper)graph regularity method.

In our new paper, using the hypergraph container method, we show that the _k_-SAT conjecture is essentially equivalent to a variant of an extremal hypergraph problem. Such extremal problems are related to hypergraph Turán density problems, which are notoriously difficult to solve in general, and for which there are lots of open problems and very few answers. 

We solved our Turán problem for all $k \le 4$, thereby confirming the conjecture for a new value $k=4$. 

Our solution to the Turán problem for $k=4$ uses a recent result in extremal graph theory by [Füredi and Maleki (2017)](https://mathscinet.ams.org/mathscinet-getitem?mr=3656340) determining the minimum density of triangular edges in a graph of given edge density.

Here is a Turán density conjecture whose resolution would imply the above conjecture for $k=5$, which is still open.

**Definition.** A *5-PDG* (*partially directed 5-graph*) is obtained from a 5-uniform hypergraph by “directing” some subset of its edges. Here every directed edge is "directed towards" one of its vertices.

**Conjecture.** There exists a constant $\theta > \log_2 3$ such that for every _n_-vertex 5-PDG with _A_ undirected edges and _B_ directed edges, if there do not exist three edges of the form
```
12345
1234 6
123 56
```
with at least one of these three edges directed towards 4, 5, or 6, then

$$A + \theta B \le (1+o(1))\binom{n}{5}.$$