---
title: "On replica symmetry of large deviations in random graphs"
date: "2012-10-29"
---

[Eyal Lubetzky](http://research.microsoft.com/~eyal) and I just uploaded to the arXiv our new paper [\`\`On replica symmetry of large deviations in random graphs.''](http://arxiv.org/abs/1210.7013) In this paper we answer the following question of [Chatterjee and Varadhan](http://arxiv.org/abs/1008.1946):

**Question.** Fix $latex {0<p<r<1}$. Let $latex {n}$ be a large integer and let $latex {G}$ be an instance of the Erdős-Rényi random graph $latex {\\mathcal G(n,p)}$ conditioned on the rare event that $latex {G}$ has at least as many triangles as the typical $latex {\\mathcal G(n,r)}$. Does $latex {G}$ look like a typical $latex {\\mathcal G(n,r)}$?

Here the Erdős-Rényi random graph $latex {\\mathcal G(n,p)}$ is formed by taking $latex {n}$ vertices and adding every possible edge independently with probability $latex {p}$. Here \`\`look like'' means close in cut-distance (but we won't give a precise definition in this blog post). In this case, saying that $latex {G}$ is close to $latex {\\mathcal G(n,r)}$ is roughly equivalent to saying that every not-too-small subset of vertices (at least constant fraction in size) of $latex {G}$ induce a subgraph with edge density close to $latex {r}$.

Another way to phrase the question is: what is the _reason_ for $latex {G}$ having too many triangles? Is it because it has an overwhelming number of edges uniformly distributed, or some fewer edges arranged in a special structure, e.g., a clique.

Via a beautiful new framework by Chatterjee and Varadhan for large deviation principles in $latex {\\mathcal G(n,p)}$, we give a complete answer to the above question.

The answer, as it turns out, depends on $latex {(p,r)}$. See the plot below. For $latex {(p,r)}$ in the blue region, the answer is yes, and for $latex {(p,r)}$ in the red region, the answer is no.

Does $latex {G}$ looks like a $latex {\\mathcal G(n,r)}$?

[![](http://yufeizhao.files.wordpress.com/2012/10/screen-shot-2012-10-28-at-10-27-11-pm.png?w=300 "Triangle phase diagram")](http://yufeizhao.files.wordpress.com/2012/10/screen-shot-2012-10-28-at-10-27-11-pm.png)

The phase transition behavior has already been observed previously by Chatterjee and Varadhan, but the determination of the exact precise phase boundary is new. Borrowing language from statistical physics, the blue region where the conditional random graph is close to $latex {\\mathcal G(n,r)}$ is called the _replica symmetric_ phase, and the red region is called the _symmetry breaking_ phase. Note that in the left part of the plot, as we fix a small value of $latex {p}$, the model experiences a double phase transition as $latex {r}$ increases from $latex {p}$ to $latex {1}$ --- starting first in the blue phase, then switches to the red phase, and then switches back to the blue phase.

More generally, our result works for any $latex {d}$-regular graph in replace of triangles. The boundary curve depends only on $latex {d}$, and they are plotted below for the first few values of $latex {d}$. In particular, this means that large deviation for triangles and 4-cycles share the same phase boundary. A pretty surprising fact! We also consider the model where we condition on the largest eigenvalue of the graph being too large, and the phase boundary also turns out to be the same as that of triangles.

We also derive similar results for large deviations in the number of linear hypergraphs in a random hypergraph.

The phase boundary for $latex {d}$-regular graphs

[![](http://yufeizhao.files.wordpress.com/2012/10/screen-shot-2012-10-28-at-10-31-59-pm.png?w=300 "blog20121028-d-reg-phase")](http://yufeizhao.files.wordpress.com/2012/10/screen-shot-2012-10-28-at-10-31-59-pm.png)

### Exponential random graphs

We also studied the [exponential random graph model](http://en.wikipedia.org/wiki/Exponential_random_graph_models). This is a widely studied graph model, motivated in part by applications in social networks. The idea is to bias the distribution of the random graph to favor those with, say, more triangles. This model has a similar flavor to the model considered above where we condition on the random graph having lots of triangles.

We consider a random graph $latex {G}$ on $latex {n}$ vertices drawn from the distribution

$latex \\displaystyle p\_\\beta(G) \\propto \\exp\\left(\\tbinom{n}{2}(\\beta\_1 t(K\_2, G) + \\beta\_2 t(K\_3, G))\\right)\\,, $

where $latex {t(K\_2, G)}$ and $latex {t(K\_3, G)}$ are the edge density and the triangle density of $latex {G}$, respectively. When $latex {\\beta\_2 = 0}$, this model coincides with the Erdős-Rényi model $latex {\\mathcal G(n,p)}$ with some $latex {p}$ depending on $latex {\\beta\_1}$. We only consider the case $latex {\\beta\_2 > 0}$, which represents a positive bias in the triangle count.

As shown by [Bhamidi, Bresler and Sly](http://projecteuclid.org/euclid.aoap/1322057318) and [Chatterjee and Diaconis](http://arxiv.org/abs/1102.2650), when $latex {n}$ is large, a typical random graph drawn from the distribution has a trivial structure --- essentially the same one as an Erdős-Rényi random graph with a suitable edge density. This somewhat disappointing conclusion accounts for some of the practical difficulties with statistical parameter estimation for such models. In our work, we propose a natural generalization that will enable the exponential model to exhibit a nontrivial structure instead of the previously observed Erdős-Rényi behavior.

Here is our generalization. Consider the exponential random graph model which includes an additional exponent $latex {\\alpha>0}$ in the triangle density term:

$latex \\displaystyle p\_{\\alpha,\\beta}(G) \\propto \\exp\\left(\\tbinom{n}{2}(\\beta\_1 t(K\_2, G) + \\beta\_2 t(K\_3, G)^\\alpha)\\right) \\, . $

When $latex {\\alpha \\geq 2/3}$, the generalized model features the Erdős-Rényi behavior, similar to the previously observed case of $latex {\\alpha = 1}$. However, for $latex {0< \\alpha < 2/3}$, there exist regions of values of $latex {(\\beta\_1, \\beta\_2)}$ for which a typical random graph drawn from this distribution has symmetry breaking, which was rather unexpected given earlier results. For example, we know that there is symmetry breaking in the shaded regions in the plots below. (The blue curve indicates a discontinuity in the model which we won't discuss in this blog post.)

Symmetry breaking in the new exponential graph model

[![](http://yufeizhao.files.wordpress.com/2012/10/screen-shot-2012-10-28-at-10-33-48-pm.png?w=1024 "blog20121028-beta-phase")](http://yufeizhao.files.wordpress.com/2012/10/screen-shot-2012-10-28-at-10-33-48-pm.png)

### Graph limits and large deviation

Our proof of the phase boundary result for large deviations in triangle counts is quite short, so I'll present it here.

The framework developed by Chatterjee and Varadhan reduces the problem of large deviations in random graphs to solving a variational problem in graph limits. _Graph limits_, also called _graphons_, are symmetric measurable functions $latex {f\\colon \[0,1\]^2 \\rightarrow \[0,1\]}$ which are, in some sense, scaling limits of adjacency matrices of graphes. The values of $latex {f}$ represent local edge densities (there are several caveats in this description but we will not go into the details here). For example, the constant function $latex {f \\equiv p}$ is the limit of $latex {\\mathcal G(n,p)}$ as $latex {n \\rightarrow \\infty}$. These objects were developed by Lovász and collaborators to understand the structure of very large graphs.

The relative entropy function $latex {h\_p}$ defined by

$latex \\displaystyle h\_p(x) := x \\log \\frac{x}{p} + (1-x) \\log \\frac{1-x}{1-p}$

for $latex p \\in (0,1)$ and $latex x \\in \[0,1\]$ is the rate function associated to the binomial distribution with probability $latex {p}$. We can extend $latex {h\_p}$ to graphons $latex {f \\colon \[0,1\]^2 \\rightarrow \[0,1\]}$ by defining

$latex \\displaystyle h\_p(f) := \\int\_{\[0,1\]^2} h\_p(f(x,y)) \\ dxdy \\, . $

We'll omit the limits of integrals from now on.

The triangle density in a graphon $latex {f}$ is given by the expression

$latex \\displaystyle t(K\_3, f) := \\int f(x,y)f(x,z)f(y,z) \\ dxdydz\\, . $

The Chatterjee-Varadhan framework reduces the problem of large deviations of triangle counts (the question stated in the beginning) to the following variational problem.

**Variational problem:** Minimize $latex {h\_p(f)}$ subject to $latex {t(K\_3, f) \\geq r^3}$.

It is known that the distribution of the random graph drawn from $latex {\\mathcal G(n,p)}$ and conditioned on the event of having triangle density at least $latex {r^3}$, in the limit as $latex {n \\rightarrow \\infty}$, converges to the set of graph limits which are the minimizers of the variational problem.

In particular we would like to know whether the constant function $latex {f \\equiv r}$ minimizes $latex {h\_p(f)}$. If it does (and if it's the unique minimizer), then we are in the replica symmetric phase, and the random graph converges to $latex {\\mathcal G(n,r)}$ in cut-distance. On the other hand, if there exists some function $latex {f}$ with a strictly smaller $latex {h\_p(f)}$ and satisfying the constraint, then we are in the symmetry breaking phase.

Thus it remains to consider the variational problem. The replica symmetry phase is determined by the following two lemmas.

**Lemma 1** _For any symmetric measurable $latex {f \\colon \[0,1\]^2 \\rightarrow \[0,1\]}$, we have_

$latex \\displaystyle t(K\_3,f)^2 \\leq \\left(\\int f(x,y)^2 \\ dxdy\\right)^3. $

_Proof:_ This is an exercise in the Cauchy-Schwarz inequality.

$latex \\displaystyle \\begin{aligned} t(K\_3, f)^2 &= \\left(\\int f(x,y)f(y,z)f(z,x) dxdydz\\right)^2 \\\\ &= \\left(\\int f(x,y) \\left(\\int f(y,z)f(z,x) dz\\right) dxdy\\right)^2 \\\\ &\\leq \\left(\\int f(x,y)^2 dxdy\\right) \\int \\left(\\int f(y,z)f(z,x) dz\\right)^2 dxdy \\\\ &\\leq \\left(\\int f(x,y)^2 dxdy\\right) \\int \\left(\\int f(y,z)^2 dz\\right) \\left(\\int f(z,x)^2 dz\\right) dxdy \\\\ &= \\left(\\int f(x,y)^2 dxdy\\right)^3. \\end{aligned}$ $latex \\Box&fg=000000$

**Lemma 2** _Let $latex {0 < p \\leq r \\leq 1}$ be such that $latex {(r^2, h\_p(r))}$ lies on the convex minorant of $latex {x \\mapsto h\_p(\\sqrt{x})}$. Then any symmetric measurable $latex {f \\colon \[0,1\]^2 \\rightarrow \[0,1\]}$ with $latex {t(K\_3,f) \\geq r^3}$ satisfies $latex {h\_p(f) \\geq h\_p(r)}$._

_Proof:_ Lemma [1](#lemcauchy) implies

$latex \\displaystyle \\int f(x,y)^2 \\ dxdy \\geq r^2. $

Define $latex {\\phi(x) = h\_p(\\sqrt{x})}$ and let $latex {\\hat\\phi}$ be the convex minorant of $latex {\\phi}$. Since $latex {\\hat\\phi}$ convex and increasing on $latex {\[p^2, 1\]}$, by Jensen's inequality we have

$latex \\begin{aligned} h\_p(f) = \\int h\_p(f(x,y)) dxdy &\\geq \\int \\hat\\phi(f(x,y)^2) dxdy\\\\ &\\geq \\hat\\phi\\left(\\int f(x,y)^2 dxdy\\right) \\geq \\hat\\phi(r^2) = \\phi(r^2) = h\_p(r). \\end{aligned} $ $latex \\Box&fg=000000$

It can be shown that the hypotheses for $latex {(p,r)}$ in Lemma [3](#lemconvex) is equivalent to

$latex \\displaystyle \\left\[1 + (r^{-1} - 1)^{1/(1-2r)}\\right\]^{-1} \\leq p \\leq r \\leq 1. $

It turns out that this region is exactly the replica symmetric phase. It is the blue region in the first plot.

To show that everything else is in the symmetry breaking phase, we need to show that the constant function $latex {f \\equiv r}$ is not a minimizer of the variational problem. The following lemma captures this fact.

**Lemma 3** _Let $latex {0 < p \\leq r \\leq 1}$ be such that $latex {(r^2, h\_p(r))}$ does not lie on the convex minorant of $latex {x \\mapsto h\_p(\\sqrt{x})}$. Then there exists a symmetric measurable $latex {f \\colon \[0,1\]^2 \\rightarrow \[0,1\]}$ with $latex {t(K\_3,f) \\geq r^3}$ and satisfying $latex {h\_p(f) < h\_p(r)}$._

_Proof:_ (Sketch) The idea is to construct $latex {f}$ by slightly perturbing the constant graphon $latex {f}$ in a way that roughly preserves the triangle count but at the same time decreases the rate function with the help of the nonconvexity of $latex {h\_p(\\sqrt{x})}$.

See figure below for an illustration of this construction. The plot of $latex {h\_p(\\sqrt{x})}$ is drawn not-to-scale to highlight its convexity features.

[![](images/screen-shot-2012-10-28-at-10-33-38-pm.png "blog20121028-breaking-construction")](http://yufeizhao.files.wordpress.com/2012/10/screen-shot-2012-10-28-at-10-33-38-pm.png)

Since $latex {(r^2, h\_p(r))}$ does not lie on the convex minorant of $latex {x\\mapsto h\_p(\\sqrt{x})}$, there necessarily exist $latex {0 \\leq r\_1 < r < r\_2 \\leq 1}$ such that the point $latex {(r^2, h\_p(r))}$ lies strictly above the line segment joining $latex {(r\_1^2, h\_p(r\_1))}$ and $latex {(r\_2^2, h\_p(r\_2))}$. Letting $latex {s}$ be such that

$latex \\displaystyle r^2 = s r\_1^2 + (1-s) r\_2^2\\,,$

we therefore have

$latex \\displaystyle s h\_p(r\_1) + (1-s) h\_p(r\_2) < h\_p(r)\\, .$

Let $latex {\\epsilon > 0}$ and define

$latex \\displaystyle \\begin{aligned} a &= s\\epsilon^2\\,, \\qquad b = (1-s)\\epsilon^2 + \\epsilon^3\\,,\\\\ I\_0 &= \[a,1-b\]\\,,\\qquad I\_1 = \[0,a\]\\,, \\qquad I\_2 = \[1-b,1\]\\,, \\end{aligned} $

noting that for $latex {a<1-b}$ for any sufficiently small $latex {\\epsilon}$. Define $latex {f\_\\epsilon \\colon \[0,1\]^2 \\rightarrow \[0,1\]}$ by

$latex \\displaystyle f\_\\epsilon(x,y) = \\begin{cases} r\_1 & \\text{if }(x,y) \\in (I\_0 \\times I\_1) \\cup (I\_1 \\times I\_0)\\,, \\\\ r\_2 & \\text{if }(x,y)\\in (I\_0 \\times I\_2) \\cup (I\_2 \\times I\_0)\\,, \\\\ r & \\text{otherwise}\\,. \\end{cases} $

It remains to check that $latex {t(K\_3,f\_\\epsilon) > r^3}$ and $latex {h\_p(f\_\\epsilon) < h\_p(r)}$ for sufficiently small $latex {\\epsilon}$. This is a straightforward calculation whose details we omit here. $latex \\Box&fg=000000$

This completes the proof the phase boundary for triangles. The proof for $latex {d}$-regular graphs is similar, except that we need to replace Lemma [1](#lemcauchy) by a generalized Hölder's inequality. We refer the reader to our paper for details.

Unfortunately, in the symmetry breaking phase where the constant function does not solve the variational problem, we do not know extremal solutions. In fact, we do not know how to solve the variational problem for any single $latex {(p,r)}$ in the symmetry breaking phase. This remains a tantalizing open problem.
