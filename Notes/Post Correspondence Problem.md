---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Computation Reducibility]], [[Turing Machines]], [[Decidable and Undecidable Problems]]

In this note we show that the phenomenon of undecidability is not confined to problems concerning automata. It is called the *Post correspondence problem* or *PCP.*

We can describe this problem easily as a type of puzzle. We begin with a collection of dominos, each containing two strings, one on each side. An individual domino looks like $$\left[\frac{a}{ab}\right]  $$and a collection of dominos looks like $$\left\{\left[\frac{b}{ca}\right], \left[\frac{a}{ab}\right] , \left[\frac{ca}{a}\right], \left[\frac{abc}{c}\right]\right\}.  $$The task is to make it a list of these dominos, repetitions permited, so that the string we get reading off the symbols on the top is the same as the string of symbols on th bottom. The list is called a *match*. An example is  $$\left[\frac{a}{ab}\right]\left[\frac{b}{ca}\right]\left[\frac{ca}{a}\right]\left[\frac{a}{ab}\right]\left[\frac{abc}{c}\right]. $$
Reading off the top string we get that $\verb|abcaaabc|$, with is the same as reading off the bottom.  For some collections of dominos finding a match may not be possible. For example, the collection$$\left\{\left[\frac{abc}{ab}\right], \left[\frac{ca}{a}\right],\left[\frac{acc}{ba}\right] \right\}  $$cannot contain a match every top string is longer than the corresponding bottom string. 

The Post correspondence problem is to determine whether a collection of dominos has a match. 

An instance of the PCP is a collection $P$ of dominos: $$P := \left\{\left[\frac{t_1}{b_1}\right], \left[\frac{t_2}{b_2}\right], \dots, \left[\frac{t_k}{b_k}\right]\right\},  $$and a match is a sequence $i_1, i_2,\dots, i_l$ where $t_{i_1} t_{i_2} \cdots t_{i_l} = b_{i_1}b_{i_2}\cdots b_{i_l}$. The problem is to determine whether $P$ has a match. Let  $$\text{PCP} := \{\langle P \rangle \mid \text{$P$ is an instance of the Post correspondence problem with a match}\}. $$
**Th:** $\text{PCP}$ is undecidable.

