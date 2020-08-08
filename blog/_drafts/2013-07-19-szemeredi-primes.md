---
title: "Recent developments on the Green-Tao theorem"
date: "2013-07-19"
---

There has quite a bit of activities around the Green-Tao theorem recently. In this blog post, I want to highlight some of these developments, focusing on the following papers, which were all posted on the arXiv in the past couple of months.

**Relative Szemerédi theorem**

- D. Conlon, J. Fox and Y. Zhao, [A relative Szemerédi theorem](http://arxiv.org/abs/1305.5440).
- Y. Zhao, [An arithmetic transference proof of a relative Szemerédi theorem](http://arxiv.org/abs/1307.4959).

**Multidimensional Szemerédi theorem in the primes**

- T. Tao and T. Ziegler, [A multi-dimensional Szemerédi theorem for the primes via a correspondence principle](http://arxiv.org/abs/1306.2886).
- B. Cook, Á. Magyar and T. Titichetrakun, [A multidimensional Szemerédi theorem in the primes](http://arxiv.org/abs/1306.3025).
- J. Fox and Y. Zhao, [A short proof of the multidimensional Szemerédi theorem in the primes](http://arxiv.org/abs/1307.4679).

\--------

We start the story with [Szemerédi’s](http://www.ams.org/mathscinet-getitem?mr=369312) famous result.

**Szemerédi’s theorem.** Every subset of integers with positive density contains arbitrarily long arithmetic progressions.

[Green and Tao](http://doi.org/10.4007/annals.2008.167.481) proved their famous theorem extending Szemerédi’s theorem to the primes.

**Green-Tao theorem.** The primes contain arbitrarily long arithmetic progressions. In fact, any subset of the primes with positive relative density contains arbitrarily long arithmetic progressions.

An important idea in Green and Tao’s work is the **transference principle**. They transfer Szemerédi’s theorem as a black box to the sparse setting, so that it can be applied to subsets of a sparse pseudorandom set of integers (in this case, some carefully designed enveloping set for the primes).

\[caption id="attachment\_220" align="aligncenter" width="300"\]![Jacob Fox, David Conlon, and myself](http://yufeizhao.files.wordpress.com/2013/07/conlonfoxzhao1.jpg?w=300) Jacob Fox, David Conlon, and me at the Erdős Centennial conference in Budapest, Hungary, July 2013.\[/caption\]

In my [recent paper](http://arxiv.org/abs/1305.5440) with David Conlon and Jacob Fox, we gave a new simplified approach to proving the Green-Tao theorem. In particular, we established a new **relative Szemerédi theorem**, which required simpler pseudorandomness hypotheses compared to Green and Tao’s original proof. Roughly speaking, a relative Szemerédi theorem is a result of the following form.

**Relative Szemerédi theorem (roughly speaking).** Let _S_ be a pseudorandom subset of integers. Then any subset of _S_ with positive relative density contains long arithmetic progressions.

The original proof in our paper followed the hypergraph approach, and in particular used the hypergraph removal lemma, a deep combinatorial result, as a black box. Subsequently, I wrote up [a short six-page note](http://arxiv.org/abs/1307.4959) showing how to prove the same result by directly transferring Szemerédi’s theorem, without going through hypergraph removal lemma. The former approach is more powerful and more general, while the latter approach is more direct and gives better quantitative bounds.

Next we shift our attention to higher dimensions. [Furstenberg and Katznelson](http://www.ams.org/mathscinet-getitem?mr=531279) proved, using ergodic-theoretic techniques, a multidimensional generalization of Szemerédi’s theorem.

**Multidimensional Szemerédi theorem** (Furstenberg and Katznelson)**.** Any subset of **Z**_d_ with positive density contains arbitrary constellations.

Here a _constellation_ means some finite set _R_ of lattice points, and the theorem says that the subset of **Z**_d_ contains some translation of a dilation of _R_.

(This result always reminds me of [a lovely scene](http://www.youtube.com/watch?v=9aSB6h4S75k) in the movie _A Beautiful Mind_ where the John Nash character traces out shapes among the stars.)

\[caption id="attachment\_218" align="aligncenter" width="300"\][!["Pick a shape" - A Beautiful Mind](http://yufeizhao.files.wordpress.com/2013/07/beautifulmind.jpg?w=300)](http://www.youtube.com/watch?v=9aSB6h4S75k) "[Pick a shape](http://www.youtube.com/watch?v=9aSB6h4S75k)" - _A Beautiful Mind_\[/caption\]

[Tao](http://www.ams.org/mathscinet-getitem?mr=2279549) proved a beautiful extension for the [Gaussian primes](http://mathworld.wolfram.com/GaussianPrime.html).

**Theorem** (Tao)**.** The Gaussian primes contain arbitrary constellations.

In that paper, Tao also made the following interesting conjecture: let **P** denote the primes. Then any subset of **P** × **P** of positive relative density contains arbitrary constellations. This statement can be viewed as a hybrid of the Green-Tao theorem and the multidimensional Szemerédi theorem. Recently this conjecture was resolved by [Tao and Ziegler](http://arxiv.org/abs/1306.2886), and independently by [Cook, Magyar, and Titichetrakun](http://arxiv.org/abs/1306.3025).

**Multidimensional Szemerédi theorem in the primes.** Let **P** denote the primes. Then any subset of **P**_d_ with positive density contains arbitrary constellations.

Terry Tao has written a [blog post](https://terrytao.wordpress.com/2013/06/13/a-multi-dimensional-szemeredi-theorem-for-the-primes-via-a-correspondence-principle/) about this new result where he describes the ideas in the proofs (so I won't repeat too much). Tao and Ziegler proved their result via ergodic theory. Their proof is about 19 pages long, and they assume as black boxes two powerful results: (1) Furstenberg and Katznelson’s multidimensional Szemerédi theorem (more precisely their equivalent ergodic-theoretic formulation) and (2) the landmark results of Green, Tao, and Ziegler on [linear equations in primes](http://www.ams.org/mathscinet-getitem?mr=2680398) (and related [work on the Mobius-nilsequences conjecture](http://www.ams.org/mathscinet-getitem?mr=2877066) and the [inverse conjecture on the Gowers norm](http://www.ams.org/mathscinet-getitem?mr=2950773)). Both these results are deep and powerful hammers.

In contrast, Cook, Magyar, and Titichetrakun proceeded differently as they develop a sparse extension of hypergraph regularity method from scratch, without assuming previous deep results. Though their paper is much longer, at 44 pages.

In a [recent paper](http://arxiv.org/abs/1307.4679) by Jacob Fox and myself, we give a new and very short proof of the same result, assuming the same tools as the Tao-Ziegler proof. Our paper is only 4 pages long, and it uses a very simple sampling argument described in two paragraphs on the first page of our paper (all the ideas are on the first page; the rest of the paper just contains the technical details spelled out). I invite you to read the first page of our paper to learn the very short proof of the theorem.
