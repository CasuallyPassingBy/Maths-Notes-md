---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Orderings]]

$R$ is a _pre-order_ on $A$ if $R$ is a reflexive and transitive relation on $A.$ $(A, R)$ is a _pre-ordered set or quasi-ordered set._

$S$ is a _strict pre-ordered_ on $A$ if $S$ is an irreflexive and transitive relation on $A$. $(A, S)$ is a _strictly pre-ordered set or strictly quasi-ordered set._

Given $(A, \lesssim)$ is a pre-ordered set, Let $\sim$ be an equivalence relation on $A$ defined by:

$$ a \sim b \iff (a \lesssim b) \land (b \lesssim a) $$

Let $\le$ be an ordering on $A/\sim$ defined as:

$$ [a] \le [b] \iff a \lesssim b $$

$\le$ is independent of representatives, chosen on the equivalence class.

This is specially useful while talking about [[Directed Sets|directed sets]]