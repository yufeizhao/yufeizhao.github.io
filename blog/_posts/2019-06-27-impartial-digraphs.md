---
title: "Impartial digraphs"
layout: post
---

I just finished a new paper, [Impartial digraphs](https://arxiv.org/abs/1906.10482), coauthored with Yunkun Zhou, who just completed his undergraduate studies at MIT and will be moving to Stanford to start his PhD this fall.

{% include image.html 
    src = "/blog/images/yunkun-zhou-2019.jpg"
    caption = "with Yunkun Zhou (R) after his MIT commencement"
%}

The problem (along with the conjecture that we proved) was proposed by Jacob Fox, Hao Huang, and Choongbum Lee. Ron Graham had also told me about this problem with much enthusiasm during tea time one afternoon at the Berkeley Simons Institute a couple of years ago, after learning about it from Jacob.

I really enjoyed working on this paper with Yunkun. The problem is natural and simple to state, the answer appears somewhat unexpected (at least initially), and the solution ended up being quite tricky yet clean, employing a variety of tools in combinatorics, ranging from analytic methods (graph limits), algebraic considerations (polynomial identities and factorization), as well basic combinatorial techniques such as bijections.

We are going to talk about **directed graphs** (which graph theorists like to abbreviate as **digraphs**). These are graphs where every edge is given an orientation.

{% include image.html 
    src = "/blog/images/impartial-0.png"
    width = "150"
%}

A **tournament** is a directed graph where there is a directed edge between every pair of vertices (think of it as recording the outcome of a round-robin tournament where every player plays against every other player).

{% include image.html 
    src = "/blog/images/impartial-1.png"
    width = "150"
%}

Given a directed graph _H_ (think of it as a pattern), we can ask: how many different copies of the pattern _H_ appear in a given tournament?

{% include image.html 
    src = "/blog/images/impartial-2.png"
%}

Look at the following 4-vertex tournament _H_. It has the following curious property: all tournaments of a fixed size contains the same number of copies of H, no matter how the edges in the tournament are oriented.

{% include image.html 
    src = "/blog/images/impartial-2a.png"
%}

Hmm, why is this true? And are there other directed graphs _H_ with the same property, namely that all tournaments of a given size contain the same number of copies of _H_?

In the good old mathematical tradition, we came up with a name for directed graphs _H_ with this curious property: we called them **impartial** (as in: impartial judges of a tournament).

Okay. So why is the above directed graph impartial? Are there any other impartial directed graphs? What are all the impartial directed graphs?

Here is a simple example of an impartial digraph:

{% include image.html 
    src = "/blog/images/impartial-4.png"
    width = "70"
%}

Here is another one:

{% include image.html 
    src = "/blog/images/impartial-5.png"
    width = "100"
%}

Indeed, given any 10-vertex tournament, we can count the number of copies of the first edge (it doesn't depend on the tournament), and then count the number of copies of the second edge among the remaining 8 vertices (it still doesn't depend on the tournament).

Once these two edges are placed in a tournament, there are two ways to join their tips, but they result in identical patterns (one flipped from the other):

{% include image.html 
    src = "/blog/images/impartial-6.png"
    width = "150"
%}

It must then follow that this directed graph is impartial as well:

{% include image.html 
    src = "/blog/images/impartial-8.png"
    width = "80"
%}

We can follow the same logic and continue this procedure, iterate, and build up even larger impartial directed graphs. Each step, take two copies of the previous tree (keeping the same edge orientations), and then add a new edge between a twin pair of vertices.

{% include image.html 
    src = "/blog/images/impartial-9.png"
    width = "150"
%}

{% include image.html 
    src = "/blog/images/impartial-10.png"
    width = "150"
%}

{% include image.html 
    src = "/blog/images/impartial-11.png"
    width = "300"
%}

{% include image.html 
    src = "/blog/images/impartial-12.png"
    width = "300"
%}

We call any directed graph that can building up as above a **recursively bridge-mirrored** **tree**.

The same argument as earlier shows that every recursively bridge-mirrored tree is impartial.

Are there other impartial digraphs? Did we miss any?

It turns out, there are actually no others. We have found them all, and that is the main result of our paper:

**Theorem.** A directed graph is impartial if and only if every component is recursively bridge-mirrored trees.

Just a word about how about this problem is related to a bigger picture. It is related to a number of other graph homomorphism inequalities that are central in extremal graph theory. It can be considered as the "equality case" for a directed analog of an open problem known as **Sidorenko's conjecture**. See [our paper](https://arxiv.org/abs/1906.10482) for some further discussions and open problems.
