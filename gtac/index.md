---
layout: single
title: "18.217 Graph Theory and Additive Combinatorics"
description: "MIT Fall 2019. Graph Theory and Additive Combinatorics, taught by Prof. Yufei Zhao"
---

18.217 Graph Theory and Additive Combinatorics
===============================================

<img src="bridge.png" width="600" height="181" style="float:right; max-width: 40%; height: auto;" class="side"
 title="The bridge between graph theory and additive combinatorics">

**Fall 2019, MIT**

_Quick links_:
[\[Homework\]](ps.pdf)
[\[Lecture notes\]](https://www.overleaf.com/read/gykfrmhpwbzm)
[\[Stellar\]](http://stellar.mit.edu/S/course/18/fa19/18.217/)

**Class meetings:** Mondays and Wednesdays 2:30--4pm in 2-190

**Lecturer:** [Yufei Zhao](http://yufeizhao.com) (see link for contact info)

**Office hours:** Instead of scheduling regular office hours, the lecturer will be generally be available in the Math Common Room (2-290) after lectures to chat and answer questions. Please email for individual appointments. Special office hours may be set up before homework due dates according to demand.

Please include "18.217" in the subject line of your emails.


## Course description

The course examines classical and modern developments in graph theory and additive combinatorics, with a focus on topics and themes that connect the two subjects. The course also introduces students to current research topics and open problems.

A foundational result in additive combinatorics is **Roth's theorem**, which says that every subset of {1, 2, ..., _n_} without a 3-term arithmetic progression contains _o_(_N_) elements. We will see a couple of different proofs of Roth's theorem: (1) a graph theoretic approach and (2) Roth's original Fourier analytic approach. A central idea in both approaches is the **dichotomy of structure versus pseudorandomness**, and it is one of the key themes of the course.

Roth's theorem laid the groundwork for many important later developments, e.g.,
- **Szemerédi's theorem.** Every set of integers of positive density contains arbitrarily long arithmetic progressions;
- **Green--Tao theorem.** The primes contain arbitrarily long arithmetic progressions.

The course will explore these and related topics, including:

- **Extremal graph theory.** What is the maximum number of edges in a triangle-free graph on _n_ vertices? What if instead we forbid cycles of length 4? At most how many edges can an _n_-vertex graph have if every edge is contained in exactly one triangle?
- **Szemerédi's regularity lemma.** A powerful tool in combinatorics that provides an approximate description/decomposition for every large graph.
- **Pseudorandom graphs.** What does it mean for some graph to resemble a random graph?
- **Graph limits.** In what sense can a sequence of graphs, increasing in size, converge to some limit object?
- **Fourier analysis in additive combinatorics.** An important technique for studying combinatorial properties in arithmetic settings, e.g., in the proof of Roth's theorem. 
- **Freiman's theorem and the structure of sum sets.** What can one say about sets _A_ such that the sum set $A + A = \\{a + a' : a,a' \in A\\}$ is small?
- **Sum-product phenomenon.** Can a set $A$ simultaneously have both small sum set $A + A$ and product set $A \cdot A$?

Although the course will be largely divided into two parts (graph theory in the first half and additive combinatorics in the second), we will emphasize the interactions between the two topics and highlight the common themes.

**Prerequisites:** Mathematical maturity at the level of a first-year math graduate student.

**Grading.** The final grade will be determined by the _minimum_ of the student's performance in the two categories:
- **Problem sets**, 4~6 problem sets
- **Writing assignments**, consisting of (1) course notes and (2) Wikipedia contributions.

There will be no exams. For borderline grades, participation may play a factor in determining the final grade. In addition, there will be a list open problems for which any significant progress/resolution may, at the discretion of the instructor, result in a grading bonus, overriding the above grading criteria.

[Student Support Services (S<sup>3</sup>) and Student Disability Services](s3)

## Course notes

[Completed notes available here as PDF](gtac.pdf)

Registered students may access the write-enabled link to the course notes from the email sent to class at the beginning of term, or via the link in [Stellar](http://stellar.mit.edu/S/course/18/fa19/18.217/).  [Read-only link to course notes on Overleaf](https://www.overleaf.com/read/gykfrmhpwbzm)

Each student taking the class for credit is expected to write course notes on one lecture (possbily in collaboration with another student, depending on course enrollement).

Please see the beginning of the document for important information regarding this writing assignment. In particular, the students responsible for writing up a lecture should:

- By the end of the day after the lecture, produce a very rough draft that that should, at the minimum, include theorem statements and sketches of proofs discussed in lecture.
- Within four days of the lecture, complete a polished version of the notes and email the instructor to set up a 30-min appointment to go over the writing.

Everyone is encouraged and expected to contribute to editing the notes.

[Notes from the previous version of the course](fa17/gtac.pdf). They may be consulted but not copied when writing the new course notes.


## Lectures

Chapter/section numbers refer to the [course notes](gtac.pdf)

- **9/9**  Introduction to the course: the bridge between graph theory and additive combinatorics. Schur's theorem and Ramsey's theorem. Highlights from additive combinatorics. §1
- **9/11** Mantel's theorem and Turán's theorem. Statement of Erdős--Stone--Simonovits theorem. §2.1--2.4
- **9/16** Forbidding a bipartite subgraph: Kővári–Sós–Turán theorem and lower bound constructions. §2.5--2.7
- **9/18** Algebraic and randomized algebraic constructions of extremal graphs without complete bipartite subgraphs. §2.7--2.8
- **9/23** Forbidding a sparse bipartite graph: dependent random choice, even cycles, clique 1-subdivision §2.9
- **9/25** Szemerédi's graph regularity lemma: statement and proof. §3.1
- **9/30** Szemerédi's graph regularity lemma: triangle counting and removal lemmas. Proof of Roth's theorem. §3.2--3.3
- **10/2** Behrend's construction of sets without 3-term arithmetic progressions. Corner's theorem. Graph embedding, counting, and removal lemmas. Proof of Erdős--Stone--Simonovits theorem. §3.4--3.5
- **10/7** Induced removal lemma. Strong graph regularity lemma. Graph property testing. §3.6--3.7
- **10/9** Hypergraph regularity and removal lemmas. Spectral proof of graph regularity lemma. §3.8--3.9
- **10/16** Pseudorandom graphs: Chung--Graham--Wilson equivalences for quasirandom graphs. Expander mixing lemma. §4.1--4.1
- **10/21** Pseudorandom graphs and spectra: Paley graphs, quasirandom Cayley graphs, Alon--Boppana bound on second eigenvalue. §4.2--4.4
- **10/23** Ramanujan graphs. Sparse regularity method. Green--Tao theorem. §4.5--4.6
- **10/28** Graph limits: introduction and statements of main results (equivalence, limit, compactness). §5.1
- **10/30** Graph limits: W-random graphs, counting lemma, weak regularity lemma, martingale convergence theorem. §5.2--5.4
- **11/4** Graph limits: compactness of the space of graphons and its applications. §5.4--5.5
- **11/6** Inequalities between graph densities. §5.6
- **11/13** Roth's theorem in finite fields: Fourier analytic proof. §6.1 
- **11/18** Roth's theorem in the integers: Fourier analytic proof. §6.2
- **11/20** Croot--Lev--Pach polynomial method proof of Roth's theorem in finite fields. Arithmetic regularity lemma. Roth's theorem with popular differences. §6.3--6.4
- **11/25** Structure of set addition: introduction to Freiman's theorem, Ruzsa triangle inequality, Plünnecke--Ruzsa inequality. §7.1--7.2
- **11/27** Structure of set addition: Ruzsa covering lemma, Freiman's theorem in groups of bounded exponent, Freiman homomorphisms, modeling lemma. §7.3--7.5
- **12/2** Structure of set addition: Bogolyubov's lemma, geometry of numbers. §7.6--7.7
- **12/4** Structure of set addition: proof of Freiman's theorem. Nonabelian Freiman problem and polynomial Freiman--Ruzsa conjecture. §7.8--7.11
- **12/9** Additive energy and Balog--Szemerédi--Gowers theorem. §7.12.
- **12/11** Sum-product problem and incidence geometry. §8
   

## Homework

[**Problem set**](ps.pdf): a list of problems for practice. A subset of these problems will be designated as to-be-turned in by 11:59pm of each due date. You should only submit the designated problems.

| Problem set | Due date (♣ tentative) | 
|:---------------:|:-----------:|
| PS 1 | Sunday September 29 | 
| PS 2 | Sunday October 13 | 
| PS 3 | Sunday October 27 | 
| PS 4 | Sunday November 10 |
| PS 5 | Sunday November 24 |
| PS 6 | Wednesday December 11  |

[Stellar/Gradebook](http://stellar.mit.edu/S/course/18/fa19/18.217/) -- primarily used for submitting and returning homework

_Submissions._ All homework submissions should be typed in LaTeX and submitted as PDF on [Stellar](http://stellar.mit.edu/S/course/18/fa19/18.217/). To make the grader's job easier, please name your file `ps#_Lastname_Firstname.pdf` (replace # by problem set number, and the rest by your name). Remember to include your name at the top of your submission. [Suggested LaTeX template for homework submissions.](https://www.overleaf.com/read/tczmqrrzbrnd)

_Late policy._ Submissions are due on Stellar by **11:59pm of each due date**. Late submissions will be penalized by 20% per each late day. For example, for an assignment due on Sunday, a submission worth _x_ points if turned in on time will be worth $0.6x$ points if submitted on Tuesday.

_Sources._ **Important!** Please acknowledge, **individually for every problem** at the beginning of each solution, a list of all collaborators and sources consulted (people, books, websites, etc.). Write `sources consulted: none` even if no sources are consulted. **Failure acknowledge sources will lead to an automatic 10% penalty**. You may not look up solutions to homework problems online or offline. 

_Collaboration policy._ You are strongly encouraged to start early and first work on the problems on your own. Reasonable collaboration is permitted, but everyone must write their solutions individually and acknowledge their collaborators.


## Wikipedia contributions

You may work in teams of sizes 1~3 to create or revise one or more articles on Wikipedia on topics related to the course (the topic does not have be one covered in the course; anything that is tangentially related is okay)

**Due date: Sunday December 1**. Please send the instructor an email (one per team) containing a short summary with links of your team’s contributions to Wikipedia

This is an open-ended assignment. The goal is to create more useful “entry points” to the subject, since Wikipedia is often among the first search results when someone Googles a term.

Quality matters more than quantity. A very rough guideline is that each person should have contributions equivalent to 30~50% of one high quality article.

Link to page for coordination sent out in email (link also available in Stellar)

## Open problems

Open problems will regularly be mentioned in the course. You are encouraged to talk to Prof. Zhao if one of these problems interests you. Any major progress/resolution of one of the open problems (e.g., leading to a significant and publishable result) would be quite exciting, and could, among other things, result in an automatic A+ grade at the instructor's discretion.

## References

Additional references for material covered in the course

**Extremal graph theory**

- David Conlon's notes on [extremal graph theory](https://www.dpmms.cam.ac.uk/~dc340/Extremal-course.html)
- Asaf Shapira's notes on [extremal graph theory](http://www.math.tau.ac.il/~asafico/ext-graph-theory/notes.pdf)
- Choongbum Lee's notes on [extremal combinatorics](http://math.mit.edu/~cb_lee/18.318/materials.html)

**Pseudorandom graphs and graph limits**

- Chapter 9 of Alon and Spencer, [The Probabilitic Method](https://www.amazon.com/gp/product/1119061954/)
- László Lovász, [Large Networks and Graph Limits](https://www.amazon.com/gp/product/0821890859/)

**Additive combinatorics**

- Ben Green's notes on [additive combinatorics](http://people.maths.ox.ac.uk/greenbj/notes.html)
- K. Soundararajan's notes on [additive combinatorics](http://math.stanford.edu/~ksound/Notes.pdf)
- Adam Sheffer's notes on [additive combinatorics](https://adamsheffer.wordpress.com/pdf-files/)
- Tao and Vu, [Additive Combinatorics](https://www.amazon.com/gp/product/0521136563/)


**Previous version of the course** [Fall 2017](fa17/)