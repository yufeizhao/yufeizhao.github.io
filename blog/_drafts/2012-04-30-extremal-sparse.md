---
title: "Extremal results for sparse pseudorandom graphs"
date: "2012-04-30"
---

[David Conlon](http://www.maths.ox.ac.uk/contact/details/conlond), [Jacob Fox](http://math.mit.edu/~fox/) and I have just uploaded to the [arXiv](http://arxiv.org/abs/1204.6645) our paper [Extremal results in sparse pseudorandom graphs](http://yufeizhao.com/papers/sparse_counting.pdf). The main advance of this paper is a sparse extension of the counting lemma associated to Szemerédi's regularity lemma, allowing us to extend a wide range of classical extremal and Ramsey results to sparse pseudorandom graphs.

An important trend in modern combinatorics research is in extending classical results to the sparse setting. For instance, [Szemerédi's theorem](http://en.wikipedia.org/wiki/Szemeredi's_theorem) says that every subset of the integers with positive density contains arbitrarily long arithmetic progressions. The celebrated result of [Green and Tao](http://dx.doi.org/10.4007/annals.2008.167.481) says that the primes also contain arbitrarily long arithmetic progressions. While the primes have zero density in the integers, they may be placed inside a pseudorandom set of \`\`almost primes'' with positive relative density. Green and Tao established a **transference principle**, allowing them to apply Szemerédi's theorem as a black box to the sparse setting. Our work has a similar theme. We establish a transference principle extending many classical extremal graph theoretic results to sparse pseudorandom graphs.

One of the most powerful tools in extremal graph theory is [Szemerédi's regularity lemma](http://bit.ly/IbOLuF). Roughly speaking, it says that every large graph can be partitioned into a bounded number of roughly equally-sized parts so that the graph is random-like between pairs of parts. With this tool in hand, many important results in extremal graph theory can be proven using a three-step recipe, known as the **regularity method**:

1. Starting with any graph $latex {G}$, apply Szemerédi's regularity lemma to obtain a regular partition;
2. Clean up the graph and create an associated reduced graph. Solve an easier problem in the reduced graph;
3. Apply the counting lemma. Profit.

The counting lemma is a result that says that the number of embeddings of a fixed graph (e.g., a triangle) into the regular partition is roughly what you would expect if the large graph were actually random. The original version of Szemerédi's regularity lemma is useful only for dense graphs. Kohayakawa and Rödl later independently developed regularity lemmas for sparse graphs. However, for sparse extensions of the applications, the counting lemma remained a key missing ingredient and an important open problem in the field. **Our main advance lies in a counting lemma that complements the sparse regularity lemma.**

In order to state our results, we need to explain what we mean by a **pseudorandom graph**. We say that a graph $latex {\\Gamma}$ is $latex {(p, \\beta)}$-**jumbled** if for all vertex subsets $latex {X}$ and $latex {Y}$ of $latex {\\Gamma}$, we have

$latex \\displaystyle \\left| e(X,Y) - p \\left| X \\right| \\left| Y \\right| \\right| \\leq \\beta \\sqrt{\\left| X \\right| \\left| Y \\right|}. $

This notion was originally introduced by Thomason. Jumbled graphs are quite ubiquitous. For example, the [Erdös-Rényi](http://en.wikipedia.org/wiki/Erdos-Renyi_model) random graph $latex {G\_{n,p}}$, formed by taking an empty graph on $latex {n}$ vertices and adding each edge independently with probability $latex {p}$, is, with high probability, $latex {(p, \\beta)}$-jumbled with $latex {\\beta = O(\\sqrt{pn})}$. We remark that many extremal and Ramsey problems on sparse random graphs have been resolved by recent breakthroughs of [Conlon and Gowers](http://arxiv.org/abs/1011.4310), and independently [Schacht](http://www.math.uni-hamburg.de/home/schacht/preprints/extremal_rs.pdf), and they also follow more generally from the KŁR conjecture, which has also been resolved very recently. However, the techniques used for random graphs do not immediately transfer over to pseudorandom graphs.

One particularly well-known class of $latex {(p, \\beta)}$-jumbled graphs is the collection of _$latex {(n, d, \\lambda)}$-graphs_. These are graphs on $latex {n}$ vertices which are $latex {d}$-regular and such that all eigenvalues of the adjacency matrix, except for the largest, are at most $latex {\\lambda}$ in absolute value. The famous [expander mixing lemma](http://en.wikipedia.org/wiki/Expander_mixing_lemma) tells us that these graphs are $latex {(p, \\beta)}$-jumbled with $latex {p = d/n}$ and $latex {\\beta = \\lambda}$. An explicit example of such a graph is the [Paley graph](http://en.wikipedia.org/wiki/Paley_graph) with vertex set $$\mathbb{Z}_p$, where $${p \\equiv 1 (\\mbox{mod } 4)}$ is prime, and edge set given by connecting $latex {x}$ and $latex {y}$ if their difference is a quadratic residue is such a graph with $latex {p = \\frac{1}{2}}$ and $latex {\\beta = O(\\sqrt{n})}$. Pseudorandom graphs have many surprising properties and applications and have recently attracted a lot of attention both in combinatorics and theoretical computer science. For more, see the wonderful survey by [Krivelevich and Sudakov](http://www.math.ucla.edu/~bsudakov/pseudo-random-survey.pdf).

Now let us discuss some of our extremal results for sparse pseudorandom graphs.

[Mantel's theorem](http://en.wikipedia.org/wiki/Turan's_theorem#Mantel.27s_theorem) tells us that every triangle-free graph $latex {G}$ on $latex {n}$ vertices has at most $latex {\\frac{n^2}{4}}$ edges. More generally, [Turán's theorem](http://en.wikipedia.org/wiki/Turan's_theorem) tells us that every $latex {K\_{r+1}}$-free graph $latex {G}$ on $latex {n}$ vertices has at most $latex {\\frac{r-1}{r}\\frac{n^2}{2}}$ edges. And even more generally, the [Erdös-Stone-Simonovits](http://en.wikipedia.org/wiki/Erdos-Stone_theorem)theorem tells us that for any fixed graph $latex {H}$, any $latex {H}$-free graph $latex {G}$ on $latex {n}$ vertices has at most

$latex \\displaystyle \\left( 1 - \\frac{1}{\\chi(H) - 1} + o(1) \\right) \\binom{n}{2} $

edges, where $latex {\\chi(H)}$ is the chromatic number of $latex {H}$. We extend this result to sparse pseudorandom graphs. In the following statement, $latex {d(H)}$ is the [degeneracy](http://en.wikipedia.org/wiki/Degeneracy_(graph_theory)) of $latex {H}$, and $latex {e(\\Gamma)}$ is the number of edges in $latex {\\Gamma}$. For specific $latex {H}$ we often have better bounds on $latex {\\beta}$, and the same is true for our other results.

**Theorem 1 (Sparse Erdös-Stone-Simonovits)** _For every graph $latex {H}$ and every $latex {\\epsilon > 0}$, there exists $latex {c > 0}$ such that if $latex {\\beta \\leq cp^{d(H) + \\frac{5}{2}} n}$ then any $latex {(p,\\beta)}$-jumbled graph $latex {\\Gamma}$ on $latex {n}$ vertices has the property that any $latex {H}$-free subgraph of $latex {\\Gamma}$ has at most_

$latex \\displaystyle \\left( 1 - \\frac{1}{\\chi(H) - 1} + o(1) \\right) e(\\Gamma). $

edges.

A basic example in [Ramsey theory](http://en.wikipedia.org/wiki/Ramsey_theory) is that for any coloring of the edges of a $latex {K\_6}$ with two colors, there is always a monochromatic triangle. More generally, [Ramsey's theorem](http://en.wikipedia.org/wiki/Ramsey's_theorem) tells us that for any graph $latex {H}$ and positive integer $latex {r}$, if $latex {n}$ is sufficiently large, then any $latex {r}$-coloring of the edges of $latex {K\_n}$ contains a monochromatic copy of $latex {H}$. We extend Ramsey's theorem to the sparse pseudorandom graphs.

**Theorem 2 (Sparse Ramsey)** _For every graph $latex {H}$ and every positive integer $latex {r \\geq 2}$, there exists $latex {c > 0}$ such that if $latex {\\beta \\leq cp^{d(H) + \\frac{5}{2}}}$ then any $latex {(p, \\beta)}$-jumbled graph $latex {\\Gamma}$ on $latex {n}$ vertices has the property that any $latex {r}$-coloring of the edges of $latex {\\Gamma}$ contains a monochromatic copy of $latex {H}$._

One of the simplest proofs of Roth's theorem (Szemerédi's theorem for 3-term arithmetic progressions) is via the triangle removal lemma, which says that every graph on $latex {n}$ vertices with at most $latex {o(n^3)}$ triangles can be made triangle-free by deleting at most $latex {o(n^2)}$ edges. More generally, the graph removal lemma states that for every fixed graph $latex {H}$ and every $latex {\\epsilon > 0}$, there exists $latex {\\delta > 0}$ such that if $latex {G}$ contains at most $latex {\\delta n^{v(H)}}$ copies of $latex {H}$ then $latex {G}$ may be made $latex {H}$-free by removing at most $latex {\\epsilon n^2}$ edges. We extend this result to the sparse setting.

**Theorem 3 (Sparse graph removal)** _For every graph $latex {H}$ and every $latex {\\epsilon > 0}$, there exist $latex {\\delta > 0}$ and $latex {c > 0}$ such that if $latex {\\beta \\leq cp^{d(H) + \\frac{5}{2}}}$ then any $latex {(p, \\beta)}$-jumbled graph $latex {\\Gamma}$ on $latex {n}$ vertices has the following property: any subgraph of $latex {\\Gamma}$ containing at most $latex {\\delta p^{e(H)}n^{v(H)}}$ copies of $latex {H}$ may be made $latex {H}$-free by removing at most $latex {\\epsilon pn^2}$ edges._

In our paper, we use the sparse graph removal result to give a sparse extension of a removal lemma for groups, which implies an extension of Roth's theorem.

The key technical result in our paper is the counting lemma for sparse pseudorandom graphs. It is the tool that allows us to transfer these classical results to the sparse setting. For a precise statement of the counting lemma, as well as discussions of further applications, we invite you to read our paper.
