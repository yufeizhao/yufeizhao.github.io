---
title: "The critical window for the classical Ramsey-Turán problem"
date: "2012-08-27"
---

_\[Update: Po-Shen Loh gave a wonderful talk in Banff about our paper. Here is the [video](http://www.birs.ca/events/2012/5-day-workshops/12w5001/videos/watch/201208201435-Loh.mp4).\]_

[Jacob Fox](http://math.mit.edu/~fox/), [Po-Shen Loh](http://www.math.cmu.edu/~ploh/) and I recently uploaded to the arXiv our new paper [\`\`The critical window for the classical Ramsey-Turán problem.''](http://arxiv.org/abs/1208.3276) This paper revisits the following celebrated Ramsey-Turán result first proved by Szemerédi in 1972.

**Theorem 1 (Szemerédi 1972)** _For every $latex {\\epsilon > 0}$, there exists a $latex {\\delta > 0}$ such that any graph on $latex {n}$ vertices containing no 4-clique and no independent set of size greater than $latex {\\delta n}$ has at most $latex {(1/8 + \\epsilon)n^2}$ edges._

[Turán's theorem](http://en.wikipedia.org/wiki/Turan's_theorem) tells us that if we just want to construct a $latex {K\_4}$-free graph on $latex {n}$ vertices with the largest possible number of edges, then we should divide the $latex {n}$ vertices into three nearly-equal parts and put in all possible edges across parts. This yields roughly $latex {n^2/3}$ edges. However, this graph contains very large independent sets with $latex {n/3}$ vertices. So the independent set restriction (which gives the \`\`Ramsey'' part of Ramsey-Turán) rules out this construction and forces the optimal graphs to take on a very different structure.

At the time of Szemerédi's 1972 result, most people believed that a $latex {K\_4}$-free graph with largest independent set of size $latex {o(n)}$ has to be much more sparse, perhaps with only $latex {o(n^2)}$ edges. So it was a surprise when, four years later, Bollobás and Erdős gave a clever geometric construction, based on the isoperimetric inequality for the high dimensional sphere, that showed that the bound given by Szemerédi is essentially optimal.

**Theorem 2 (Bollobás and Erdős 1976)** _There exists a $latex {K\_4}$-free graph on $latex {n}$ vertices with largest independent set of size $latex {o(n)}$ and having $latex {(1/8 - o(1))n^2}$ edges._

Bollobás and Erdős asked what happens in the critical window, when the number of edges is about $latex {n^2/8}$. This problem has received considerable attention (e.g., it was featured in a paper by Erdős from 1990 titled [\`\`Some of my favourite unsolved problems''](http://dx.doi.org/10.1017/CBO9780511983917.039)). One of the difficulties here is that Szemerédi's original proof used the regularity lemma, which is a powerful tool but one that unfortunately gives very poor parameter dependencies. To obtain results for the Ramsey-Turán problem at the desired precision, a regularity-free proof is needed. We give a new proof of the classical Ramsey-Turán result that avoids the use of regularity. This allows us to obtain much better and in fact nearly-optimal dependencies for the classical Ramsey-Turán problem in the critical window near $latex {n^2/8}$ edges, and solve several longstanding open problems in this area.

[Szemerédi's regularity lemma](http://en.wikipedia.org/wiki/Szemeredi_regularity_lemma) is a universal structural result about large dense graphs, and it acts as a powerful microscope for studying the asymptotic regimes of extremal problems. Yet this power comes at the cost of limited resolution outside of the very far asymptotic regime, as the regularity lemma's quantitative bounds necessarily involve tower-type dependencies. An important direction of research in this area has been to find alternatives to regularity-based proofs, partly in order to obtain better bounds, but also to better understand the power and limitations of the regularity method. Szemerédi's proof of the Ramsey-Turán problem is historically the first application of the regularity lemma. Originally the regularity implied a doubly-exponentials-type dependence of $latex {\\delta}$ on $latex {\\epsilon}$ (a weaker version of regularity was used then). A natural question is: **what is the correct dependence between $latex {\\delta}$ and $latex {\\epsilon}$?** Our regularity-free proof of this result significantly improves the dependencies of the parameters. **We show that there is a linear dependence between $latex {\\delta}$ and $latex {\\epsilon}$**, which is tight up to a constant factor.

For the lower bound to the $latex {K\_4}$ Ramsey-Turán problem, we modify the construction of Bollobás and Erdős to slightly boost the edge density to just over $latex {n^2/8}$. We can answer the following previously open questions about the critical window.

1. (Bollobás and Erdős 1976) Is it true that for each $latex {\\eta>0}$ there is an $latex {\\epsilon>0}$ such that for each $latex {n}$ sufficiently large there is a graph with $latex {n}$ vertices, independence number at most $latex {\\eta n}$, and at least $latex {(1/8+\\epsilon)n^2}$ edges?
2. (Bollobás and Erdős 1976) Is it true that for every $latex {n}$, there is a $latex {K\_4}$-free graph with $latex {n}$ vertices, independence number $latex {o(n)}$, and at least $latex {n^2/8}$ edges?
3. (Erdős, Hajnal, Simonovits, Sós and Szemerédi 1993) Is it true for some constant $latex {c>0}$ that every $latex {K\_4}$-free graph on $latex {n}$ vertices with no independent set of size larger than $latex {n/\\log n}$ has at most $latex {(1/8 - c) n^2}$ edges?

In our paper, we show that the answers to the questions are: yes, yes, and no.

Bollobás and Erdős drew attention to the interesting transition point of exactly $latex {n^2/8}$ edges. Thus far, the best result for this regime was a lower bound on the independence number of $latex {n e^{-O(\\sqrt{\\log n})}}$ by Sudakov. The proof relies on a powerful probabilistic technique known as [dependent random choice](http://arxiv.org/abs/0909.3271).

By introducing a new twist on the dependent random choice technique, we substantially improve this lower bound on the independence number at the critical point.

**Theorem 3** _There is an absolute positive constant $latex {c}$ such that every $latex {n}$-vertex graph with at least $latex {n^2/8}$ edges contains a copy of $latex {K\_4}$ or an independent set of size greater than $latex {c n \\cdot \\frac{\\log \\log n}{\\log n}}$._

By modifying the construction of Bollobás and Erdős we obtain the following almost-matching lower bound at the $latex {n^2/8}$ critical point.

**Theorem 4** _There is an absolute positive constant $latex {c'}$ such that for each positive integer $latex {n}$, there is an $latex {n}$-vertex $latex {K\_4}$-free graph with at least $latex {\\frac{n^2}{8}}$ edges and independence number at most $latex {c' n \\cdot \\frac{(\\log \\log n)^{3/2}}{(\\log n)^{1/2}}}$._

We summarize the results in the critical window in the following theorem. For a graph $latex {H}$ and positive integers $latex {n}$ and $latex {m}$, the Ramsey-Turán number $latex {{\\bf RT}(n,H,m)}$ is the maximum number of edges a graph $latex {G}$ on $latex {n}$ vertices with independence number less than $latex {m}$ can have without containing $latex {H}$ as a subgraph. All of the bounds, except for the first result in the first part, which is due to Sudakov, are new. We write $latex {f(n) \\ll g(n)}$ to indicate that $latex {f(n)/g(n) \\rightarrow 0}$ as $latex {n \\rightarrow \\infty}$.

**Theorem 5** _We have the following estimates. Here $latex {c}$ and $latex {c'}$ are absolute constants._

1\. If $latex {m = e^{-\\omega\\left((\\log n)^{1/2}\\right)}n}$, then $latex {{\\bf RT}(n,K\_4,m) = o(n^2)}$;

while if $latex {m=e^{-o\\left((\\log n / \\log \\log n)^{1/2}\\right)}n}$, then $latex {{\\bf RT}(n,K\_4,m) \\geq \\left(1/8-o(1)\\right)n^2}$.

2\. If $latex {m = c n \\cdot \\frac{\\log \\log n}{\\log n}}$, then $latex {{\\bf RT}(n,K\_4,m) \\leq n^2/8}$;

while if $latex {m=c' n \\cdot \\frac{(\\log \\log n)^{3/2}}{(\\log n)^{1/2}}}$, then $latex {{\\bf RT}(n,K\_4,m) \\geq n^2/8}$.

3\. If $latex {\\frac{(\\log \\log n)^{3/2}}{(\\log n)^{1/2}}\\cdot n \\ll m \\ll n}$, we have

$latex \\displaystyle \\frac{n^2}{8}+\\left(\\frac{1}{2}-o(1)\\right)m n \\leq {\\bf RT}(n,K\_4,m)\\leq \\frac{n^2}{8}+\\frac{3}{2}mn.$
