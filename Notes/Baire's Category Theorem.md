---
tags:
  - Topology
---
Subject: [[Topology]]
Links : [[Special Sets in Topological Spaces]],
## $F_\sigma$ and $G_\delta$ sets

A subset $G$ of a topological space $(X, \tau)$ is $G_\delta$ it it is the intersection of a countable family of open subsets of $X$. $F\subseteq X$ is $F_\sigma$ if it is the union of a countable family of closed subsets of $X$

The complement of a $G_\delta$ set is a $F_\sigma$ set, and $F_\sigma$ set is a $G_\delta$ set.

A $F_\sigma$ set is the increasing union of closed sets, and a $G_\delta$ set is the intersection of decreasing open subsets. 

In a metric space $(X, d)$, then every closed set is $G_\delta$, and every open set is $F_\sigma$.

## First and Second Category Subspaces

A subspace $Y$ of $X$ is of *first category*, also called meagre, if it is the union of a countable family of nowhere dense subsets of $X$. When the subspace $Y$ is not of first category on $X$, we call it that is of *second category* on $X$. 

A topological space $X$ is of the first/second category in itself if is first/second category on $X$. 

We see that any subset of a first category space is also of first category, and the countable union of first category sets is also of first category.

Any countable set on a dense-in-itself space where every set with only one point is closed, is of the first category.

We have that a space $X$ is of second category in itself, iff for every sequence $\{U_n \mid n \in \Bbb N\}$ of open and dense subsets of $X$, we have that $\bigcap \{U_n \mid n \in \Bbb N\}\ne \varnothing$ 

## Baire's Category Theorem for Metric Spaces

Let $X$ be a complete metric space and $\{A_n \mid n \in \Bbb N\}$ be a sequence of nowhere dense sets on $X$. Then we can see that $X\setminus \{A_n \mid n \in \Bbb N\}$ is dense in $X$

We say that a topological space $X$ is a *Baire space* if for every sequence of open and dense sets $\{U_n \mid n \in \Bbb N\}$ , we have that $\bigcap \{U_n \mid n \in \Bbb N\}$ is dense in $X$.

Every Baire space is of the second category

Every complete metric space is a Baire space

Every complete metric space is of the second category

Let $X$ be a Baire space iff for every countable family of dense sets $\{G_n \mid n \in \Bbb N\}$ that are $G_\delta$ on $X$, we have that $\bigcap \{G_n \mid n \in \Bbb N\}$ us dense subset of $X$.

We have that the set $\Bbb Q$ is not a $G_\delta$ subset on the metric of $\Bbb R$