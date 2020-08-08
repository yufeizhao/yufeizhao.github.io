---
title: "Upper tails for triangles in sparse random graphs"
date: "2014-02-26"
---

[Eyal Lubetzky](http://research.microsoft.com/en-us/um/people/eyal/) and I just finished and uploaded to the arXiv our new paper _[On the variational problem for upper tails of triangle counts in sparse random graphs](http://arxiv.org/abs/1402.6011)_. This paper concerns the following question:

**The upper tail problem for triangles.** What is the probability that the number of triangles in an Erdős-Rényi graph graph $latex {\\mathcal{G}\_{n,p}}$ is at least twice its mean, or more generally, larger than the mean by a factor of $latex {1 + \\delta}$?

This problem has a fairly rich history, and it is considered a difficult problem in probabilistic combinatorics. In a 2002 paper titled _[The infamous upper tail](http://www.ams.org/mathscinet-getitem?mr=1900611)_, Janson and Ruciński surveyed the progress on the problem and described its challenges (they also considered the upper tail problem more generally for any subgraph $latex {H}$, but we focus on triangles here). Research towards the solution of this problem has led to new techniques for bounding probabilities of rare events. Note that in contrast, the lower tail problem --- finding the probability of getting too _few_ triangles --- is comparatively easier.

Here we consider the case when _p_ tends to zero as _n_ grows (the dense case, where $latex {p}$ is fixed, leads to an interesting variational problem involving graph limits, as shown by a seminal work of [Chatterjee and Varadhan](http://www.ams.org/mathscinet-getitem?mr=2825532) --- see my previous [blog post](http://yufeizhao.wordpress.com/2012/10/28/replica-symmetry/)). It is not too hard to describe what the answer _should_ be in the sparse setting. Suppose we arbitrarily select a set of $latex {k = \\delta^{1/3}np}$ vertices and force it to be a clique, that is, we force all edges between these _k_ vertices to be present in the random graph --- the probability \`\`cost'' of this constraint is $latex {p^{\\binom{k}{2}} = p^{(\\delta^{2/3}/2 + o(1))n^2p^2}}$ --- the cliques gives us roughly an additional $latex {\\binom{k}{3} = (\\delta + o(1))\\binom{n}{3} p^3}$ triangles, thereby boosting the total number of triangles in the graph by a factor of $latex {1 + \\delta}$ from the mean, which is $latex {\\binom{n}{3}p^3}$.

Let _t(G_) denote the triangle density in a graph _G_, i.e., the number of triangles in _G_ as a fraction of the maximum possible number $latex {\\binom{n}{3}}$ of triangles. The above argument shows that the upper tail probability satisfies

$latex \\displaystyle \\mathbb{P}(t(\\mathcal{G}\_{n,p}) \\geq (1 + \\delta)p^3) \\geq \\exp\\Big(-(\\tfrac12 \\delta^{2/3} +o(1))n^2 p^2 \\log(1/p)\\Big). $

Is this lower bound tight? That is, can we find a matching upper bound for the upper tail probability? This is precisely the _infamous upper tail_ problem mentioned earlier. For a long time there was no satisfactory upper bound anywhere close to the lower bound. A breakthrough by [Kim and Vu](http://www.ams.org/mathscinet-getitem?mr=2035874) in 2004 gave an upper bound of the form $latex {\\exp(-c n^2p^2)}$. However, this still leaves a missing factor of log(1/_p_) in the exponent. This problem was finally settled in 2012 by [Chatterjee](http://www.ams.org/mathscinet-getitem?mr=2925306) and independently by [DeMarco and Kahn](http://www.ams.org/mathscinet-getitem?mr=2925307). They showed that the exponent in the probability has order $latex {n^2p^2 \\log(1/p)}$, thereby filling in the "missing log."

Now we know the correct order in the exponent, what remains unknown is the constant in front of the $latex {n^2p^2 \\log(1/p)}$. In a very recent breakthrough by [Chatterjee and Dembo](http://arxiv.org/abs/1401.3495) (the preprint was released just January this year), they provided a framework that reduces this large deviation problem to a certain variational problem, at least in the range when $latex {p \\geq n^{-\\alpha}}$ for some explicit (though small) $latex {\\alpha > 0}$. The variational problem is the natural one associated to this problem, and it is expected to hold for much sparser random graphs as well.

Eyal and I have been working on this variational problem for quite some time, starting with our [previous paper](http://arxiv.org/abs/1210.7013) where we studied the problem in the dense setting (constant $latex {p}$) and determined the phase diagram for replica symmetry. In our new paper, we solve this variational problem in the sparse regime. Combining the solution of this variational problem with the new results of Chatterjee and Dembo, this determines the correct asymptotic in the exponent of the upper tail probabilities, at least when $latex {n^{-\\alpha} \\ll p \\ll 1}$. For fixed $latex {\\delta > 0}$, we can now prove that

$latex \\displaystyle \\mathbb{P}(t(\\mathcal{G}\_{n,p}) \\geq 1 + \\delta) = \\exp\\Big(-(C\_\\delta+o(1))n^2 p^2 \\log(1/p)\\Big). $

where we determine the constant in the exponent to be

$latex \\displaystyle C\_\\delta = \\min\\Big\\{\\tfrac12 \\delta^{2/3}, \\tfrac13 \\delta\\Big\\}. $

We described earlier the story behind the $latex {\\tfrac12 \\delta^{2/3}}$ term (by forcing a clique of size $latex {\\delta^{1/3}np}$). Where does the other term, $latex {\\tfrac13 \\delta}$, come from? It turns out there is another way to get a lots of triangles relatively cheaply, at least when $latex {p \\gg n^{-1/2}}$: forcing a set of $latex {\\ell = \\frac13 \\delta np^2}$ vertices to be connected to all other vertices. This has probability $latex {p^{\\ell(n - \\ell)} = p^{(\\delta/3 + o(1))n^2p^2}}$. The first construction (forcing a clique) competes with the second construction (forcing a complete bipartite graph): the former is preferable when $latex {\\delta > 27/8}$ and the latter is preferable when $latex {\\delta < 27/8}$. It turns out, as we show in our paper, that these are essentially the only constructions.
