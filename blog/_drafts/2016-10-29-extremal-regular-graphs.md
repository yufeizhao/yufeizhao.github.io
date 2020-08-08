---
title: "Extremal regular graphs"
date: "2016-10-29"
---

_This post is adapted from my new expository survey [Extremal regular graphs: independent sets and graph homomorphisms](https://arxiv.org/abs/1610.09210)._

The earliest result in **extremal graph theory** is usually credited to [Mantel](https://goo.gl/1HqcUo), who proved, in 1907, that a graph on $latex {n}$ vertices with no triangles contains at most $latex {n^2/4}$ edges, where the maximum is achieved for a complete bipartite graph with half of the vertices on one side and half on the other side. Much more is now known about the subject. While I initially encountered Mantel's theorem as a high school student preparing for math contests, my first in-depth exposure to extremal graph theory was from taking a course by David Conlon during my year reading Part III at Cambridge (one can find excellent [course notes](https://www.dpmms.cam.ac.uk/~dc340/Extremal-course.html) on his website).

We seem to know less about sparse graphs (a general mantra in combinatorics, it seems). Let us focus on _$latex {d}$-regular_ graphs, which are graphs where every vertex has degree $latex {d}$.

![C4](images/c4.png)

The cycle of length 4 has a total of 7 independent sets.

An _independent set_ in a graph is a subset of vertices with no two adjacent. Many combinatorial problems can be reformulated in terms of independent sets by setting up a graph where edges represent forbidden relations.

**Question.** _In the family of $latex {d}$-regular graph of the same size, which graph has the most number of independent sets?_

This question was raised by Andrew Granville in the 1988 Number Theory Conference at Banff, in an effort to resolve a problem in combinatorial number theory, namely the [Cameron–-Erdős conjecture](https://en.wikipedia.org/wiki/Cameron%E2%80%93Erd%C5%91s_conjecture) on the number of sum-free sets. The question appeared first in print in [a paper by Noga Alon](http://www.ams.org/mathscinet-getitem?mr=1135215), who proved an asymptotic upper bound and speculated that, at least when $latex {n}$ is divisible by $latex {2d}$, the maximum should be attained by a disjoint union of complete bipartite graphs $latex {K\_{d,d}}$.

Some ten years later, [Jeff Kahn](http://www.ams.org/mathscinet-getitem?mr=1841642) arrived at the same conjecture while studying a problem arising from statistical physics. Using a beautiful entropy argument, Kahn proved the conjecture under the additional assumption that the graph is already bipartite.

Fast forward another nearly ten years. In the summer of 2009, during my last summer as an undergraduate, I spent a fun and productive summer attending [Joe Gallian's REU](http://www.d.umn.edu/~jgallian/REU.html) in Duluth, MN (a fantastic program, by the way!), and there [I showed](http://yufeizhao.com/papers/indep_reg.pdf) that Kahn's theorem can be extended to all regular graphs, not just bipartite ones.

Here is the theorem statement. We write $latex {I(G)}$ to denote the set of independent sets in $latex {G}$, and $latex {i(G) := |I(G)|}$ the number of independent sets in $latex {G}$.

**Theorem (Kahn, Z.)** _If $latex {G}$ is an $latex {n}$-vertex $latex {d}$-regular graph, then_

$latex \\displaystyle i(G) \\le i(K\_{d,d})^{n/(2d)} = (2^{d+1} - 1)^{n/(2d)}$.

In the survey, I provide an exposition of the proofs of these two theorems as well as a discussion of subsequent developments. Notably, [Davies, Jenssen, Perkins, and Roberts](https://arxiv.org/abs/1508.04675) recently gave a brand new proof of the above theorems by introducing a powerful new technique, called the _occupancy method_, inspired by ideas in statistical physics, and it already has a number of surprising new consequences.

On a personal level, I am pleased to see this topic gaining renewed interest. (Also, somewhat to my chagrin, my undergraduate paper, according to Google Scholar, still remains my most cited paper to date.)

I shall close this blog post with one of my favorite open problems in this area.

Let $latex {c\_q(G)}$ denote the number of proper $latex {q}$-colorings of $latex {G}$, i.e., coloring the vertices of $latex {G}$ with $latex {q}$ colors, so that no two adjacent vertices receive the same color.

**Conjecture.** _If $latex {G}$ is an $latex {n}$-vertex $latex {d}$-regular graph, and $latex {q \\ge 3}$, then_

$latex \\displaystyle c\_q(G) \\le c\_q(K\_{d,d})^{n/(2d)}$.

I was pleased to learn from Will Perkins, who gave a talk at Oxford last week, that he, along with Davies, Jenssen, and Roberts, recently [proved the conjecture for 3-regular graphs](https://arxiv.org/abs/1610.08496). The proof uses the occupancy method that they developed earlier. The method is reminiscent of the [flag algebra](http://www.ams.org/notices/201310/rnoti-p1324.pdf) machinery developed by Razborov some ten years ago for solving extremal problems in dense graphs. The new method can be seen as some kind of \`\`flag algebra for sparse graphs''. I find this development quite exciting, and I expect that more news will come.

![hom_coloring.png](images/hom_coloring.png)

Graph homomorphisms from _G_ to _Kq_ correspond to proper colorings of vertices of _G_ with _q_ colors.
