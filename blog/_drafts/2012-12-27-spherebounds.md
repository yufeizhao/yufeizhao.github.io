---
title: "Sphere packing bounds via spherical codes"
date: "2012-12-27"
---

[Henry Cohn](http://research.microsoft.com/~cohn) and I just uploaded to the arXiv our paper [\`\`Sphere packing bounds via spherical codes.''](http://arxiv.org/abs/1212.5966) _\[Update: Henry gave a wonderful talk about our paper at the IAS. A video of the talk is available [here](http://video.ias.edu/1213/analysis/0122-HenryCohn).\]_

![KeplerConjecture](http://yufeizhao.files.wordpress.com/2012/12/keplerconjecture.png?w=300)What's the most space-efficient way to arrange a collection of identical balls? This is known as the [sphere packing problem](http://en.wikipedia.org/wiki/Sphere_packing). It is a very difficult problem with a long and interesting history. This problem in 3-dimensions is known as [Kepler conjecture](http://en.wikipedia.org/wiki/Kepler_conjecture), which says that the the face-centered cubic formation does best. This is basically how grocers stack oranges. The seemingly innocent Kepler conjecture turned out to be extremely difficult, and it was only solved in the late 1990's by Thomas Hales who gave a very complex proof involving massive computer-aided calculations. I've included a few article links at the end of this blog post on the history and background of the sphere packing problem.

Now, what about sphere packing in higher dimensions? Unfortunately, we know very little about what happens beyond three dimensions. No proof of optimality is known in any higher dimension, and there are only a few dozen dimensions in which there are even plausible conjectures for the densest packing. In dimensions 8 and 24 there are upper bounds that are extremely close to the conjectured optima, thanks to the works of Cohn, Elkies, and Kumar \[[1](http://arxiv.org/abs/math.MG/0110009),[2](http://arxiv.org/abs/math.MG/0408174),[3](http://arxiv.org/abs/math.MG/0403263)\] (dimensions 8 and 24 are somehow special because of the existence of highly symmetric lattices known as the $latex {E\_8}$ lattice in dimension 8 and the Leech lattice in dimension 24). However, in most dimensions we must be content with much cruder bounds.

The current state of art for sphere packing density upper bounds is more or less as follows:

- In dimensions 1, 2, 3, the exact upper bound is known. The result for dimension 3 is due to [Hales](http://bit.ly/12Q1EVv).
- In low dimensions, namely 4 to 42, [Cohn and Elkies](http://arxiv.org/abs/math.MG/0110009) improved previous record by Rogers, although there were some recent improvements in dimensions 4,5,6,7,9 by [de Laat, Filho, and Vallentin](http://arxiv.org/abs/1206.2608) using techniques of semidefinite programming.
- In all high dimensions, namely 43 and above, the best bounds are due to Kabatiansky and Levenshtein in 1978 and have not been improved since then.

The purpose of our of paper is fourfold:

1. We give a small improvement over the 1978 bounds of Kabatiansky and Levenshtein in high dimensions by giving a simple modification of their geometric argument relating spherical codes to sphere packings.
2. Kabatiansky and Levenshtein derived their bounds by first formulating a linear program for proving upper bounds on spherical codes. Cohn and Elkies found a more direct approach to bounding sphere packing densities, with no need to consider spherical codes. However, despite the excellent performance in low dimensions, the asymptotic behavior of the Cohn-Elkies bound is far from obvious and it has been unclear whether it improves on, or even matches, the Kabatiansky-Levenshtein bound asymptotically. In our paper, we show that in every dimension $latex {n}$, the Cohn-Elkies linear program can always match the Kabatiansky-Levenshtein approach. This further demonstrates the power of the linear programming bound for sphere packing.
3. We prove an analogue of the Kabatiansky-Levenshtein bound in hyperbolic space. The resulting bound is exponentially better than the best bound previously known in hyperbolic space.
4. We develop the theory of hyperbolic linear programming bounds and prove that they too subsume the Kabatiansky-Levenshtein approach. Packing in hyperbolic space is much more difficult to handle than in Euclidean space, primarily because the volume of an expanding ball grows exponentially with its radius (instead of polynomially as in the case of Euclidean space), so we that cannot neglect boundary fluctuations. In fact, it is a non-trivial matter to even define the density of a packing (there are [examples](http://www.ma.utexas.edu/users/radin/reviews/boroczky.html) of packings for which any reasonable definition of density should yield two different answers).

* * *

**Further reading**

Some articles on the history and background of the sphere packing problem:

Popular audience:

- [Oddballs: It's easier to pack spheres in some dimensions than in others](http://www.sciencenews.org/view/feature/id/5472/description/Oddballs) by E. Klarreich in _Science News_ ([another link](http://bit.ly/UniY14)).
- [The 24-dimensional greengrocer](http://dx.doi.org/doi:10.1038/424895a) by I. Stewart in _Nature._
- [A fine mess](http://www.ma.utexas.edu/users/radin/reviews/newscientist2.html) by D. Mackenzie in _New Scientist._
- [Kepler’s Conjecture and Hales' Proof](http://www.ams.org/notices/200501/rev-morgan.pdf) A book review by F. Morgan in _Notices of the AMS_.

General mathematical audience:

- [Cannonballs and Honeycombs](http://www.ams.org/notices/200004/fea-hales.pdf) by T. Hales in _Notices of the AMS._
- [Kissing Numbers, Sphere Packings, and Some Unexpected Proofs](http://www.ams.org/notices/200408/fea-pfender.pdf) by F. Pfender and G.M. Ziegler in _Notices of the AMS._
