---
title: "Joints tightened"
layout: blogpost
description: Tight bounds for the joints problem in incidence geometry
---

I’m happy to announce a new paper titled [Joints tightened](https://arxiv.org/abs/1911.08605) coauthored with Hung-Hsun Hans Yu, an undergraduate student at MIT. In this paper, we determine the tight constant in the joints problem.  

{% include blog_image
    src = "hans-yu-2019.jpg"
    width = "300"
    caption = "Hung-Hsun Hans Yu"
%}

The **joints problem** is a classic problem in **incidence geometry**. A typical question in incidence geometry concerns what kinds of configurations can be built using just points and lines.

Suppose you are allowed to draw _L_ lines in space. What is the maximum possible number of points that lie on three lines (let’s call these points "triple intersections" for now)?

It turns out this is not a great question, since you can “cheat” by drawing a 2-dimensional picture from a grid as below. This configuration of _L_ lines has $$\Theta(L^2)$$ triple intersections, and you cannot do much better since _L_ lines have at most $L^2$ intersections.

{% include blog_image
    src = "joints-grid-diagonal.png"
    width = "200"
    caption = "Not a joints configurations"
%}

The issue with the above example is that it is really a 2-dimensional configuration, whereas we really want to ask a 3-dimensional question. One way to make the problem much more interesting is only count "truly 3-dimensional" intersection points.

Given a collection of lines in space, we define a **joint** to be a point that is contained in three of our lines and not all lying on the same plane.

{% include blog_image
    src = "joints-3-planes.png"
    width = "200"
    caption = "A joint"
%}

**Joints problem.** What is the maximum number of joints that can be formed by _L_ lines in 3-dimensional space?

The joints problem was raised in [early 1990’s](https://doi.org/10.1016/0925-7721(92)90009-H), and it turned out to be a very interesting problem! Besides its intrinsic interest as a combinatorial geometry problem, it also caught the attention of analysts as the joints problem is connected to the [Kakeya problem](https://en.wikipedia.org/wiki/Kakeya_set), a central problem in analysis (this connection was popularized by [Wolff](http://amathe.web.elte.hu/modern/wolff_review.pdf)).

Here are some examples of configurations of lines that have a lot of joints.

**Example 1.** The easiest example to visualize is by considering a $$k \times k \times k$$ grid of lines, which has $$L = 3k^2$$ lines and $$J = k^3 = (L/3)^{3/2}$$ joints:  


{% include blog_image
    src = "joint-3d-grid.png"
    width = "300"
    caption = "A grid of joints"
%}


**Example 2.** Actually, there is another example that has even more joints (by a constant factor). Think about a tetrahedron, formed by 4 faces (planes), and whose edges form 6 lines, and the vertices form 4 joints. We can generalize the tetrahedron example by taking _k_ generic planes in space, and have the planes pairwise intersect to make $$L = \binom{k}{2}$$ lines, and triplewise intersect to make $$J = \binom{k}{3}$$ joints. (This example appeared in the [original paper](https://doi.org/10.1016/0925-7721(92)90009-H) on the joints problem.)

{% include blog_image
    src = "joints-optimal.png"
    width = "300"
    caption = "Planes, lines, and joints"
%}

In both examples, the number of joints is $$\Theta(L^{3/2})$$. A matching upper bound on the number of joints turned out to be much less obvious. A stunning breakthrough took place in 2008 when [Guth and Katz](https://arxiv.org/abs/0812.1043) proved an $$O(L^{3/2})$$ upper bound on the number of joints in using the polynomial method. Their solution was partly inspired by [Dvir’s stunning solution](https://arxiv.org/abs/0803.2336) to the finite field Kakeya problem, and it was also a precursor to Guth and Katz’s subsequent celebrated [solution of the Erdős distinct distances problem](https://arxiv.org/abs/1011.4105).

Larry Guth conjectured in his book [The Polynomial Methods in Combinatorics](https://bookstore.ams.org/ulect-64/) that the second example above is best possible. I first learned about this very nice conjecture as a graduate student in Guth’s class on the polynomial method.

The main result of our paper is a new improved upper bound on the joints problem, matching the constant in the second example above. More precisely, we prove that _L_ lines in space make at most $$\frac{\sqrt{2}}{3}L^{3/2}$$ joints, thereby confirming Guth’s conjecture up to a $$1+o(1)$$ factor. Our results also hold in arbitrary dimensions and over arbitrary fields.

It was quite unexpected to us that such a tight bound can even be proved, especially given how long it took just to obtain an upper bound of the right order of magnitude on the joints problem. In pretty much all other classical problems in incidence geometry (i.e., the [Szemerédi–Trotter theorem](https://en.wikipedia.org/wiki/Szemer%C3%A9di%E2%80%93Trotter_theorem)), the optimal constant factor is not known. In fact, our result might be the first one in incidence geometry that obtains a tight constant factor.
