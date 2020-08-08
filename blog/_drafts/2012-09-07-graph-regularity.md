---
title: "Graph regularity"
date: "2012-09-07"
---

In this blog post I will give a brief introduction to Szemerédi's Regularity Lemma, a powerful tool in graph theory. The post is based on a talk I gave earlier today at a graduate student lunch seminar.

Consider the following problem. Suppose you're given a [very large graph](http://arxiv.org/abs/0902.0132). The graph has so many vertices that you won't be able to access all of them. But nevertheless you want to find out certain things about the graph. These situations come up in real world applications. Perhaps we would like to know something about a social network, e.g., Facebook, but we don't have the resource to go through every single node, as there are simply too many of them. For the purpose of this blog post though, we won't talk about applications and instead stick to the mathematics.

Suppose we are interested answering the following question about the very large graph:

_Is the graph triangle-free?_

Think of the given graph as a black box. We have the following access to the graph: we are allowed to randomly sample some number of vertices and be told of all the edges between these vertices.

Can we achieve the desired goal? Well, if the graph contains, say, only a single triangle, then it's pretty much a hopeless task, since we are almost certainly never going to find the single needle in this giant haystack through random sampling. So we have to be content with a more modest objective.

_Can we distinguish a graph that's triangle-free from a graph that is $latex {\\epsilon}$-far from triangle-free?_

Being $latex {\\epsilon}$-far from a property means that we would have to add/delete at least $latex {\\epsilon n^2}$ edges from the graph to make it satisfy that property. Here $latex {n}$ is the number of vertices in the very large graph. Note that this model puts us in the setting of dense graphs, i.e., graphs with $latex {\\Omega(n^2)}$ edges.

This problem we know how to solve. The algorithm is very straightforward: sample some constant number of vertices, and check to see if you see any triangles.

**Algorithm:** Sample $latex {C\_\\epsilon}$ (some constant depending on $latex {\\epsilon}$) vertices

- If a triangle is detected, then output that the graph is not triangle-free.
- If no triangle is detected, then output that the graph is triangle-free

If the given graph is triangle-free, then clearly we won't ever detect any triangles, so the algorithm always outputs the correct answer. But what if the given graph is not triangle-free? We said earlier that in this case we'll assume the graph is $latex {\\epsilon}$-far from triangle free. We want the algorithm to detect at least one triangle so that it can give the correct. However, the randomized nature of the algorithm means that there will be some probability that the output will be erroneous. We are claiming that this error probability is small.

This claim seems very innocent. Essentially we need to show that if a graph cannot be made triangle-free by deleting a small number of edges, then it must not contain very many triangles. If you haven't seen this claim before, you might think that it's something that would follow from some easy deductions, and you might be tempted to work it out yourself. However, be warned that you will almost certainly not succeed. The claim is indeed correct, but it is far from trivial.

The proof of the correctness of the algorithm essentially boils down to the following result due to Ruzsa and Szemerédi from 1978.

**Theorem 1 (Triangle Removal Lemma)** _For every $latex {\\epsilon > 0}$ there exists a $latex {\\delta > 0}$ such that if a graph on $latex {n}$ vertices is $latex {\\epsilon}$-far from triangle-free then it contains at least $latex {\\delta n^3}$ triangles._

The Triangle Removal Lemma implies that the algorithm is outputs the correct answer with high probability. Indeed, if there at least $latex {\\delta n^3}$ triangles, then by sampling enough triples of vertices (depending on $latex {\\delta}$), we are likely to encounter at least one triangle.

The result is called Triangle Removal Lemma because it is usually stated in the contrapositive: if a graph has fewer than $latex {\\delta n^3}$ triangles, then it can be made triangle-free by deleting some $latex {\\epsilon n^2}$ edges.

The Triangle Removal Lemma is far from trivial, and you probably won't be able to do it with just bare hands. In fact, until some [recent work of Jacob Fox](http://arxiv.org/abs/1006.1300), the only way anyone knew how to prove the triangle removal lemma was via Szemerédi's Regularity Lemma.

So what is Szemerédi's Regularity Lemma?

Roughly speaking, Szemerédi's Regularity Lemma says that **the vertex set of every large graph can be decomposed into a bounded a number of roughly equally-sized parts so that the graph is random-like between most pairs of parts**. It gives a structural classification of all large dense graphs, and it has proven to be a very powerful tool in combinatorics.

Let me now explain the regularity lemma in more detail. What do we mean by \`\`random-like?'' This notion is captured in the following definition, which basically says that the edge density between two fairly large vertex subsets should be approximately the same as the overall edge density.

For (disjoint) vertex sets $latex {U}$ and $latex {V}$, let $latex {e(U,V)}$ denote the number of edges with one endpoint in $latex {U}$ and the other endpoint in $latex {V}$, and let $latex {d(U,V) := \\frac{e(U,V)}{|U| |V|}}$ denote the edge density between $latex {U}$ and $latex {V}$.

**Definition 2** _A bipartite graph between $latex {X}$ and $latex {Y}$ is said to be **$latex {\\epsilon}$-regular** if for all $latex {U \\subset X}$ and $latex {V \\subset Y}$ with $latex {|U| \\geq \\epsilon |X|}$ and $latex {|V| \\geq \\epsilon |Y|}$ we have $latex {|d(U,V) - d(X,Y)| < \\epsilon}$._

![](images/blog20120907_graph_regularity-fig-bipartite.png "blog20120907_graph_regularity-fig-bipartite")

Now that we know what it means for a bipartite graph to be $latex {\\epsilon}$-regular, we can now say what an $latex {\\epsilon}$-regular partition means.

**Definition 3** _A partition of vertices of a graph into $latex {k}$ equal parts (the difference in size of two parts is at most 1) is said to be **$latex {\\epsilon}$-regular** if all but $latex {\\epsilon k^2}$ pairs of parts induce $latex {\\epsilon}$-regular bipartite graphs._

Now we are ready to state Szemerédi's Regularity Lemma.

**Szemerédi's Regularity Lemma** _For every $latex {\\epsilon > 0}$, there is some $latex {M}$ such that every graph has an $latex {\\epsilon}$-regular partition into at most $latex {M}$ parts._

![](images/blog20120907_graph_regularity-fig-partition.png "blog20120907_graph_regularity-fig-partition") A key point here is that the number of parts does not depend on the size of the graph---so this is indeed a result that can be applied to very large graphs. The bound $latex {M}$ on the number of parts depends only on $latex {\\epsilon}$ (what is this dependence? We'll come back to this point later). Also note that the edge-densities do not have to be the same for all the bipartite graphs.

So why is Szemerédi's Regularity Lemma a useful result? What can a regular partition do for you?

Intuitively the regularity lemma partitions the graph into some number of parts so that the graph, in some sense, behaves as if it were a random graph with prescribed densities between the parts. For example, in a random graph with edge density $latex {p}$, we would expect the triangle density to be roughly $latex {p^3}$. The same turns out to be true for the regular partition.

One benefit of a regular partition is that we have a **counting lemma**, which roughly says that the number of embeddings of small graphs into a regular partition is roughly the same as if there underlying graph were generated randomly. For example, without going into the details, the **triangle counting lemma** says that if we have three parts $latex {X, Y, Z}$, and the graph is $latex {\\epsilon}$-regular between each pair, then the number of triangles $latex {xyz}$ with $latex {x \\in X}$, $latex {y \\in Y}$ and $latex {z \\in Z}$ is roughly $latex {d(X, Y) d(X, Z) d(Y,Z) |X| |Y| |Z|}$, the same as if the underlying graph were random.

![](images/blog20120907_graph_regularity-fig-triangle.png "blog20120907_graph_regularity-fig-triangle")

With the powerful tool of Szemerédi's Regularity Lemma at hand, we can now sketch a short proof of the Triangle Removal Lemma.

_Proof sketch of Triangle Removal Lemma._ Suppose $latex {G}$ is $latex {\\epsilon}$-far from triangle-free. Apply Szemerédi's regularity lemma and obtain an $latex {\\frac{\\epsilon}{8}}$-regular partition of the vertices of $latex {G}$ into at most $latex {M}$ parts. \`\`Clean up'' the graph by deleting all edges that are (1) internal to any part, or (2) between any irregular pair of parts, or (3) between any two parts with edge density less than $latex {\\frac{\\epsilon}{4}}$. In each step we delete at most $latex {\\frac{\\epsilon}{4}n^2}$ edges, so we've deleted fewer than $latex {\\epsilon n^2}$ edges. Since $latex {G}$ was $latex {\\epsilon}$-far from triangle-free, it follows that even after deleting these edges, some triangle must have still remained, say between parts $latex {X}$, $latex {Y}$, $latex {Z}$. We have not deleted any edges between the parts $latex {X}$, $latex {Y}$, $latex {Z}$, and the bipartite graphs between them are regular and have density bounded from below, and it therefore follows by the triangle counting lemma that there approximately $latex {d(X,Y)d(Y,Z)d(X,Z)|X||Y||Z| \\geq (\\epsilon/4)^3(n/M)^3}$ triangles (to make this rigorous we need to give a lower bound on the number of triangles). By choosing $latex {\\delta}$ appropriately, say $latex {\\delta = (\\epsilon/4)^3(1/M)^3/2}$, we see that $latex {G}$ contains at least $latex {\\delta n^3}$ triangles.   $latex {\\square}$

The example I just gave about testing for triangles in a very large graph is known as property testing. It is a well-studied topic in computer science.

Next I want to show how to deduce Roth's Theorem from the Triangle Removal Lemma.

**Roth's Theorem** _Every subset of the integers with positive density contains a 3-term arithmetic progression._

Roth's Theorem is a special case of [Szemerédi's Theorem](http://en.wikipedia.org/wiki/Szemeredi's_theorem), which states that every subset of the integers with positive density contains arbitrarily long arithmetic progressions. Szemerédi proved his theorem in 1975 using his regularity lemma. Several new proofs have been discovered since then.

To prove Roth's Theorem using the Triangle Removal Lemma, we need to construct an auxiliary graph so that the 3-term arithmetic progressions are encoded by triangles in the graph.

_Proof sketch of Roth's Theorem._ Suppose $latex {S \\subset {\\mathbb Z}}$ has (upper) density at least $latex {2\\epsilon}$, and that $latex {S}$ does not contain any 3-term arithmetic progression. There exists arbitrarily large $latex {n}$ so that at least $latex {\\epsilon}$ fraction of the elements of $latex {\\{-n+1, -n+2,\\dots,n\\}}$ are in $latex {S}$. Let $latex {A = S \\cap \\{-n+1, -n+2, \\dots, n\\}}$. Construct a tripartite graph with vertex sets $latex {X, Y, Z}$, each with $latex {6n}$ nodes labeled by $latex {\\{-3n+1, -3n+2, \\dots, 3n\\}}$. Connect $latex {x \\in X}$ with $latex {y \\in Y}$ if and only if $latex {y-x \\in A}$. Connect $latex {y \\in Y}$ with $latex {z \\in Z}$ if and only if $latex {z -y \\in A}$. Finally connect $latex {x \\in X}$ with $latex {z \\in Z}$ if and only if $latex {(z-x)/2 \\in A}$.

[![](images/blog20120907_graph_regularity-fig-roth.png "blog20120907_graph_regularity-fig-roth")](http://yufeizhao.files.wordpress.com/2012/09/blog20120907_graph_regularity-fig-roth.png)

Then $latex {x \\in X}$, $latex {y \\in Y}$, $latex {z \\in Z}$ form a triangle if and only if $latex {y-x,(z-x)/2, z-y \\in A}$. The numbers $latex {y-x, (z-x)/2, z-y}$ form an arithmetic progression, and since $latex {A}$ contains no 3-term arithmetic progressions, these three numbers must equal. It follows all triangles in $latex {G}$ have the form $latex {x, x+a, x+2a}$, where $latex {a \\in A}$, and these triangles are all edge disjoint. Since there are at least $latex {2n|A| \\geq 4\\epsilon n^2}$ such edge-disjoint triangles, it must be $latex {\\frac{4\\epsilon}{18^3}}$-far from triangle-free (recall that there are $latex {18n}$ vertices in our graph), and hence by the Triangle Removal Lemma, for some $latex {\\delta > 0}$ (depending on $latex {\\epsilon}$ only), there at least $latex {\\delta n^3}$ triangles. But there are only at most $latex {6n|A| \\leq 12n^2}$ triangles (all of the form $latex {x, x+a, x+2a}$), and $latex {12 n^2 < \\delta n^3}$ for $latex {n}$ sufficiently large. This is a contradiction.  $latex {\\square}$

Graph regularity is an active research area. Let me conclude by outlining some of the directions and goals in this area.

1. **Understanding the limitations of the regularity lemma**In the regularity partition, how does the number of parts depend on the regularity parameter $latex {\\epsilon}$? As it turns out, the dependence is very bad. The proof of Szemerédi's Regularity Lemma gives us
    
    $latex \\displaystyle 2^{2^{2^{\\dots^{2^2}}}} \\bigg\\rbrace \\quad \\text{tower of 2's of height } O(\\epsilon^{-5}) $
    
    This bound is simply astronomical. Could it be possible that maaybe another proof of Szemerédi's Regularity Lemma could give us a more reasonable bound? It turns out that the answer is no. As shown by [Gowers](https://www.dpmms.cam.ac.uk/~wtg10/gafasz.ps) and [Conlon-Fox](http://arxiv.org/abs/1107.4829), in general an $latex {\\epsilon}$-regular partition necessarily requires essentially this number of parts (up to the exponent of $latex {\\epsilon}$ in the height of the tower). So the tower-type bound is needed. As a consequence, any application of the regularity lemma necessarily yields terrible bounds and quantitative dependencies. This is a major drawback of the regularity lemma.
2. **Extending the regularity lemma.**Szemerédi's regularity lemma gave us a terrible bound. However, in some applications we do not need the full strength of conclusion the regularity lemma. Weaker versions of the regularity lemma have been formulated that gives much better bounds on the number of parts (e.g., $latex {2^{O(\\epsilon^{-2})}}$) at the cost of weaker conclusions. Examples of these weaker regularity lemmas include [Frieze-Kannan](http://www.math.cmu.edu/~af1p/Texfiles/regular.pdf) and [Duke-Lefman-Rödl](http://epubs.siam.org/doi/abs/10.1137/S0097539793247634). In the other direction, there is a stronger version of the regularity lemma, given by [Alon, Fischer, Krivelevich, and Szegedy](http://www.cs.tau.ac.il/~nogaa/PDFS/testn12.pdf), where a stronger conclusion is obtained at the cost of even worse bounds. The bound required for the strong regularity lemma is of wowzer type, which is one level higher than tower of exponentials in the Ackermann hierarchy. At the extreme end of this direction, if we really don't care about bounds on the number of parts, there is an analytic version of the Szemerédi's Regularity Lemma by [Lovász and Szegedy](http://oldwww.cs.elte.hu/~lovasz/analyst.pdf), which can be stated beautifully as the compactness of some space of graph limits.As we saw, Roth's Theorem follows rather quickly from triangle removal lemma. There is a similarly short deduction of the more general Szemerédi's Theorem on $latex {k}$-term arithmetic progressions if we have removal lemmas for hypergraphs. **Hypergraph regularity** turns out to be a much more difficult matter, and it was developed independently by [Gowers](https://www.dpmms.cam.ac.uk/~wtg10/hypersimple4.pdf) and [Rödl-Schacht](http://www.math.uni-hamburg.de/home/schacht/2005/pnas.pdf). It is not easy to even state the conclusion of the hypergraph regularity lemma.
    
    The original version of Szemerédi's Regularity Lemma was only useful for dense graphs, and it is natural to extend it to **sparse graphs**. An extension of the regularity lemma for sparse graphs was developed independently by Kohayakawa and Rödl in the 90's, but it was only recently, in a work by [Conlon, Fox, and myself](http://yufeizhao.wordpress.com/2012/04/30/extremal-sparse/), that a general counting lemma for the sparse extension was developed.
3. **Finding new applications of regularity.**The regularity lemma has shown to be a very powerful tool in combinatorics as well as other areas. In this post I talked about a couple of the applications, but there are many more old and new applications in variety of settings, too numerous to be listed here. We are still very much interested in discover new and clever applications of graph regularity.
4. **Avoiding regularity.**How can we get rid of regularity in the proofs that use regularity? This might initially strike as a strange goal given how much we're trying to promote the power of regularity. However, as mentioned earlier, one of the main drawbacks of regularity is that it gives terrible bounds. A theorem originally proven with regularity might not actually need regularity for its proof, and an alternate proof might give much better and perhaps more useful bounds. For example, [Gowers' Fourier analytic proof](http://www.cs.umd.edu/~gasarch/vdw/sz-thm-gowers-proof.pdf) of Szemerédi's Theorem gave us much better bounds than those from Szemerédi's original proof. [Fox's new proof](http://arxiv.org/abs/1006.1300) of the Triangle Removal Lemma gives a better bound than the one from regularity and thus it shows that Szemerédi's Regularity Lemma is fundamentally not necessarily for the proof. Another example is the recently work by [Fox, Loh, and myself](http://yufeizhao.wordpress.com/2012/08/26/ramsey-turan/) on a result of Szemerédi on the classical Ramsey-Turán problem.

**Further readings**

- For more background on the regularity lemma, see the excellent surveys by [Komlós and Simonovits](http://www.ma.huji.ac.il/~ehudf/courses/Ramsey04/regularitysurvey.ps) and [Rodl and Schacht](http://www.math.uni-hamburg.de/home/schacht/2010/reg_survey.pdf).
- I formally learned Szemerédi's Regularity Lemma through David Conlon's Cambridge Part III course on Extremal Graph Theory. His notes are available [here](https://www.dpmms.cam.ac.uk/~dc340/Extremal-course.html).
