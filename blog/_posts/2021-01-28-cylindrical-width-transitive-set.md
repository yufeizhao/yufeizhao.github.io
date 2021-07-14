---
title: "The cylindrical width of transitive sets"
layout: blog
image: /blog/images/transitive-set-width.png
description: A finite transitive subset of a high dimensional sphere lies close to a subspace.
---

The high dimensional sphere comes many surprising and counterintuitive features. Here is one of them.

We say that a subset $X$ of the unit sphere in $\mathbb{R}^d$ is _transitive_ if, informally, one cannot distinguish one point of $X$ from another if we are allowed to rotate/reflect. 
Formally, we say that $X$ is transitive if the group of isometries of $X$ acts transitively on it. This is equivalent to saying that $X$ is the orbit of some point under the action of some subgroup of the orthogonal group.

Perhaps you, like me, can only visualize in three-dimensions. Here are some examples:
* Every regular polytope (platonic solid) is transitive.
* Start with an arbitrary vector, and consider all points obtained by permuting its coordinates, as well as switching the signs of some of the coordinates. The resulting set is transitive (this is a generalization of the [permutahedron](https://en.wikipedia.org/wiki/Permutohedron).) A specific example is given below.
* The whole sphere itself is transitive

The finite examples look like they can be fairly spread out on the sphere. 
However, this intuition turns out to be completely wrong in high dimensions.
All _finite_ transitive sets in high dimensions have small width, meaning that they lie close to some hyperplane (in sharp contrast to the whole unit sphere, which has width 2).

I had conjectured the following statement, which was proved by Ben Green.

**Theorem** ([Green](https://dev.arxiv.org/abs/1802.01904)). Every finite transitive set of unit vectors in $\mathbb{R}^d$ lies within distance $O\bigl(\frac{1}{\sqrt{\log d}}\bigr)$ of some hyperplane.

{% include blog_image
    src = "transitive-set-width.png"
    width = "500"
    caption = "A finite transitive set lies close to a hyperplane"
%}

This bound is actually tight for the example obtained by taking all signings and permutations of the unit vectors

$$
\frac{1}{\sqrt{H_d}}\Biggl(\pm 1, \frac{\pm  1}{\sqrt{2}}, \frac{\pm  1}{\sqrt{3}}, \ldots,  \frac{\pm 1}{\sqrt{d}}\Biggr)
$$

where

$$
H_d = 1 + \frac{1}{2} + \cdots + \frac{1}{d} \sim \log d.
$$

Green's proof, among other things, uses the classification of finite simple groups.

### Our new results: finite transitive sets have small cylindrical width

In our new paper, [The cylindrical width of transitive sets](https://arxiv.org/abs/2101.11207), coauthored with Ashwin Sah and Mehtaab Sawhney, we generalize Green's result to show that not only do transitive sets lie close to a hyperplane, but they also lie close to some codimension-$k$ subspace for every $k$ that is not too large. 

**Theorem** ([Sah--Sawhney--Zhao](https://arxiv.org/abs/2101.11207)). There exists some constant $C$ so that for every $1 \le k \le d/(\log d)^C$, every finite transitive set of unit vectors in $\mathbb{R}^d$ lies within distance $O\bigl(\frac{1}{\sqrt{\log (d/k)}}\bigr)$ of codimension-$k$ subspace.

The bound $O\bigl(\frac{1}{\sqrt{\log (d/k)}}\bigr)$ is tight up to a constant factor. We conjecture that the hypothesis $1 \le k \le d/(\log d)^C$ can be removed:

**Conjecture.** For every $1 \le k \le d$, every finite transitive set of unit vectors in $\mathbb{R}^d$ lies within distance $O\bigl(\frac{1}{\sqrt{\log (2d/k)}}\bigr)$ of codimension-$k$ subspace.

Finally, we conjecture that not only do finite transitive sets lie close to subspaces, but they can be completely contained in a small cube. All examples known to us are consistent with this conjecture, even though I still find it very counterintuitive.

**Conjecture** (Finite transitive sets lie in a small cube). Every finite transitive set of unit vectors in $\mathbb{R}^d$ is contained in a cube of width $O\bigl(\frac{1}{\sqrt{\log d}}\bigr)$.

Even proving a bound of $o(1)$ (as $d\to \infty$) would be quite interesting.

Both conjectures are generalizations of Green's result, but the relationship between the two conjectures is unclear. 