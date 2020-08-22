---
title: "A reverse Sidorenko inequality"
layout: blog---

Together with undergraduates Ashwin Sah, Mehtaab Sawhney, and David Stoner (the same team that [proved Kahn's conjecture on independent sets that I blogged about earlier]({% post_url /blog/2018-05-12-the-number-of-independent-sets-in-an-irregular-graph %}),
we are excited to announce our new paper [A reverse Sidorenko inequality](https://arxiv.org/abs/1809.09462). This paper solves several open problems concerning graph colorings and homomorphisms, including one of my favorite problems regarding maximizing the number of _q_-colorings in a _d_-regular graph. I had previously [blogged](https://yufeizhao.wordpress.com/2016/10/29/extremal-regular-graphs/) about some of these problems.

It has been truly a pleasure working with Ashwin, Mehtaab, and David on this project. I have learned so much from them.

{% include image.html 
    src = "/blog/images/hom_coloring.png"
    width = "400"
%}

Here are some highlights of our new results.

### 1. Graph colorings.

 Among _d_-regular graphs, which graph has the most number of proper _q_\-colorings, exponentially normalized by the number of vertices of _G_?

We show that the extremal graph is the complete bipartite graph $$K_{d,d}$$ (or disjoint unions thereof, as taking disjoint copies does not change the quantity due to the normalization).

### 2. Graph homomorphisms.

Among _d_-regular graphs, which triangle-free graph _G_ has the most number of homomorphisms into a fixed _H_, again exponentially normalized by the number of vertices of _G_?

We show that the extremal graph _G_ is the complete bipartite graph $$K_{d,d}$$.

The triangle-free hypothesis on _G_ is best possible in general. For certain specific _H,_ such as $$K_q$$, corresponding to proper _q_-colorings as earlier, the triangle-free hypothesis can be dropped. It remains a wide open problem to determine for which _H_ can one drop the triangle-free hypothesis on _G_.

### 3. Partition functions of Ferromagnetic spin models.

Among _d_-regular graphs, which graph maximizes the log-partition function per vertex of a given Ferromagnetic spin model (e.g., Ising model)?

We show that the extremal graph is the clique $$K_{d+1}$$.

For each setting, we establish our results more generally for irregular graphs as well, similar to [our earlier work on independent sets]({% post_url /blog/2018-05-12-the-number-of-independent-sets-in-an-irregular-graph %}).

Our results can be interpreted as a reverse form of the inequality in **Sidorenko's conjecture**, an important open problem in graph theory stating a certain positive correlation on two-variable functions.

One can also view our results as a graphical analog of the **Brascamp–Lieb inequalities**, a central result in analysis.

This paper resolves one of my favorite open problems on this topic (the number of graph colorings). It also points us to many other open problems. Let me conclude by highlighting one of them (mentioned in #2 earlier). I'll state it in a simpler form for _d_-regular graphs, but it can be stated more generally as well.

**Open problem.** Classify all _H_ with the following property: among _d_-regular graphs _G_, the number of homomorphisms from _G_ to _H_, exponentially normalized by the number of vertices of _G_, is maximized by $$G = K_{d,d}$$.

Our results show that $$H = K_q$$ works, even when some of its vertices are looped. Generalizing this case, we conjecture that all antiferromagnetic models _H_ have the same property (though we know that this would not be the complete class, even if true).
