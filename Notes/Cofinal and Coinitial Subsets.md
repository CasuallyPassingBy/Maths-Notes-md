---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Binary Relations]], [[Orderings]]

Let $\le$ be a homogeneous relation on a set $A$. A subset $B$ is said to be *cofinal* or *frequent*, with respect to $\le$ if it satisfies that:
$$
	\forall a \in A \exists b \in B[a \le b]
$$
A subset that is not frequent is called *infrequent*. Apparently this is used a lot in something called [[Directed Sets|directed sets]].

The cofinal relation over partially ordered sets is reflexive: every partially ordered set is cofinal in itself. If $B$ is a cofinal subset of partially ordered set $A$, and $C$ is a cofinal subset of $B$, then $C$ is cofinal on $A$.

For partially ordered sets with maximal elements, every cofinal subset must contain all maximal element. Similarly, for partially ordered sets with a greatest element, a subset is cofinal iff contains that greatest element. 

A subset $B\subseteq A$ is said to be coinitial if it satisfies the following condition:
$$
	\forall a \in A \exists b \in B[b \le a]
$$
This is the order-theoretic dual of the notion of cofinal subset.