---
title: "Schildkraut: Equiangular lines and large multiplicity of fixed second eigenvalue"
layout: blogpost
image: /blog/images/carl-schildkraut-2023.jpg
description: Graph with high second eigenvalue multiplicity for a fixed eigenvalue
twitter_large_image: true
---

{% include blog_image
    src = "carl-schildkraut-2023.jpg"
    width = "200"
    caption = "Carl Schildkraut"
%}


 
I am excited to share and discuss the latest work by an MIT undergraduate senior, Carl Schildkraut, titled [Equiangular lines and large multiplicity of fixed second eigenvalue](https://arxiv.org/abs/2302.12230). In his paper, Carl offers new constructions on two related problems:
* equiangular lines,
* graphs with high second eigenvalue multiplicities.

### Equiangular lines 

In my [previous work on equiangular lines (with Zilin Jiang, Jonathan Tidor, Yuan Yao, and Shengtong Zhang)](https://mathscinet.ams.org/mathscinet-getitem?mr=4334975) (previously report on [this blog]({% post_url /blog/2019-07-30-equiangular-lines-with-a-fixed-angle %}) and [MIT News](https://news.mit.edu/2021/mathematicians-solve-old-geometry-problem-equiangular-lines-1004)), we solved the following problem:

**Problem (Equiangular lines with a fixed angle).** For a given fixed angle, in sufficiently large dimensions, determine the maximum possible number of lines that can be pairwise separated by the given angle.

The answer can be phrased in terms of the **spectral radius order $k(\lambda)$**, defined to be the smallest integer $k$ so that there exists a $k$-vertex graph $G$ whose adjacency matrix has top eigenvalue exactly $\lambda$. Furthermore, we define $k(\lambda) = \infty$ if no such graph $G$ exists.

**Theorem** ([Jiang--Tidor--Yao--Zhang--Zhao](https://mathscinet.ams.org/mathscinet-getitem?mr=4334975)). For $\alpha \in (0,1)$. Let $\lambda = (1-\alpha)/(2\alpha)$ and let $k(\lambda)$ be its spectral radius order. Then the maximum number $N_\alpha(d)$ of equiangular lines in $\mathbb{R}^d$ with common angle $\arccos \alpha$ satisfies:  
(a) If $k(\lambda) < \infty$, then $N_\alpha(d) = \lfloor k(d-1) / (k-1) \rfloor$ for all sufficiently large $d$;  
(b) If $k(\lambda) = \infty$, then $N_\alpha(d) = d + o(d)$ as $d \to \infty$.

In particular, this result determines the first order growth rate of $N_\alpha(d)$ for all $\alpha$. Even better, when the spectral radius order is finite, our result determines the answer exactly in all sufficiently large dimensions. (There is a tantalizing open question on how high the dimension needs to be.) However, when the spectral radius order is infinite, our result gives only an asymptotic $d + o(d)$. Can we hope for a more precise answer?

[Jiang and Polyanskii](https://mathscinet.ams.org/mathscinet-getitem?mr=4093893) conjectured that $N_\alpha(d) = d + O_\lambda(1)$ when $k(\lambda) = \infty$, i.e., the $o(d)$ error term should be at most constant depending on $\lambda$. They verified this conjecture when $\lambda$ is either (a) not a totally real algebraic integer or (b) a totally really algebraic integer that is not the largest among its Galois conjugates. We also reiterated this conjecture in [our paper](https://arxiv.org/abs/1907.12466).

Carl Schildkraut’s new paper gives a counterexample to these conjectures.

**Theorem** ([Schildkraut](https://arxiv.org/abs/2302.12230)). There exist infinitely many $\alpha$ such that $N_{\alpha}(d) \ge d + \Omega_\alpha(\log \log d)$.

I found this result to be quite surprising. I had expected the opposite to be true.

### Second eigenvalue multiplicity

One of the key ingredients in our equiangular lines paper is a bound on the second eigenvalue multiplicity.

**Theorem** ([Jiang-Tidor-Yao-Zhang-Zhao](https://mathscinet.ams.org/mathscinet-getitem?mr=4334975)). The adjacency matrix of every connected $n$-vertex graph with maximum degree $\Delta$ has second eigenvalue multiplicity at most $O_\Delta(n/\log \log n)$.

The fact that the second eigenvalue multiplicity is sublinear in the number of vertices plays a crucial role in our solution to the equiangular lines with a fixed angle problem.

The second eigenvalue multiplicity bound leaves many open questions. 

How tight is the bound? The quantitative bound is the bottleneck being able to improve the “sufficiently large dimension” part of the equiangular lines result. The $O_\Delta(n/\log\log n)$ bound is still best known (though, see the work of [McKenzie--Rasmussen--Srivastava](https://mathscinet.ams.org/mathscinet-getitem?mr=4398851) for an improvement to $O_\Delta(n/(\log n)^c)$ in the case of regular graphs). See my work with [Milan Haiman, Carl Schildkraut, Shengtong Zhang](https://mathscinet.ams.org/mathscinet-getitem?mr=4499595) (previously reported on [this blog]({% post_url /blog/2021-09-28-eig-mult %})) for the current best lower bound constructions, giving $\Omega(\sqrt{n /\log n})$.

Here is a question relevant to the equiangular lines problem with a fixed angle (appearing as Question 6.4 in [our equiangular lines paper](https://arxiv.org/abs/1907.12466)):

**Question.** Fix $\Delta, \lambda >0$. What is the maximum multiplicity that $\lambda$ as the second eigenvalue of a connected $n$-vertex graph with maximum degree at most $\Delta$?

We suggested the possibility that perhaps the answer is always at most a constant depending on $\Delta$ and $\lambda$. I really thought that the answer should be bounded. Carl’s paper shows otherwise.

**Theorem** ([Schildkraut](https://arxiv.org/abs/2302.12230)). For infinitely many values of $\lambda$ and $d$, there exist sequences of connected $d$-regular graphs whose second eigenvalue is exactly $d$ and has multiplicity at least $\Omega_{d, \lambda}(\log \log n)$.

So now we know that the answer to the earlier question is between $\Omega(\log\log n)$ and $O(n/\log \log n)$. There is still a huge gap.

Carl managed to get his construction many families of $\lambda$, including some with $k(\lambda) = \infty$, which implies his equiangular lines result stated earlier.

Carl’s construction is quite elegant, incorporating several clever ideas in spectral graph theory. One of the ideas used is the 2-lift technique from the seminal [Bilu-Linial paper](https://mathscinet.ams.org/mathscinet-getitem?mr=2279667). This is a way to transform a graph into another graph with twice as many vertices and in a way that allows us to control the spectrum. 

For Carl’s construction, in order to perform the 2-lift and control the eigenvalues, given a $d$-regular bipartite graph, he needs to select a regular subgraph in a way that is somewhat random. There needs to be enough independent sources of randomness so that he can apply concentration bounds. He does this by, roughly speaking, partitioning the graph into short even cycles, and then for each even cycle, independently choosing one of the two alternating sets of edges.

There is another catch, which is that in order for his concentration bounds to go through, he needs to first make the graph large enough so that the relevant eigenvectors are all somewhat flat. He does this by repeatedly performing the Ramanujan lift from the seminal work of [Marcus--Spielman--Srivastava](https://mathscinet.ams.org/mathscinet-getitem?mr=3374962). (Carl doesn’t need the full strength of the MSS result, but why resist applying such a beautiful theorem.)

This is really nice construction. These interesting ideas will surely lead to further developments in spectral graph theory.
