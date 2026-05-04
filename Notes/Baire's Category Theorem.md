---
tags:
  - Topology
---
Subject: [[Topology]]
Links : [[Special Sets in Topological Spaces]], [[Perfect Spaces]], [[Product Topology]], [[Borel Sets]]

## First and Second Category Subspaces

A subspace $Y$ of $X$ is of *first category*, also called meagre, if it is the union of a countable family of nowhere dense subsets of $X$. When the subspace $Y$ is not of first category on $X$, we call it that is of *second category* on $X$. 

A topological space $X$ is of the first/second category in itself if is first/second category on $X$. 

We see that any subset of a first category space is also of first category, and the countable union of first category sets is also of first category.

Any countable set on a dense-in-itself space where every set with only one point is closed, is of the first category.

Let us note, that the boundary of a closed set is nowhere dense in the space. A subset of a topological space is nowhere dense in that space iff it is a subset of the boundary of a closed set.

A subset $A$ of a topological space $X$ is *nearly open* if there are subsets $M_1$ and $M_2$ of the first category of $X$ such that $(A \setminus M_1) \cup M_2$ is open. 

Every Borel set of a topological space $X$ is nearly open. 

We have that a space $X$ is of second category in itself, iff for every sequence $\{U_n \mid n \in \Bbb N\}$ of open and dense subsets of $X$, we have that $\bigcap \{U_n \mid n \in \Bbb N\}\ne \varnothing$ 

We say that a topological space $X$ is a *Baire space* if for every sequence of open and dense sets $\{U_n \mid n \in \Bbb N\}$ , we have that $\bigcap \{U_n \mid n \in \Bbb N\}$ is dense in $X$.

**Prop:** In a Baire space, every meagre subset has dense complement. 

# Baire's Category Theorem for Metric Spaces

Let $X$ be a complete metric space and $\{A_n \mid n \in \Bbb N\}$ be a sequence of nowhere dense sets on $X$. Then we can see that $X\setminus \bigcup \{A_n \mid n \in \Bbb N\}$ is dense in $X$

Every Baire space is of the second category

Every complete metric space is a Baire space

Every complete metric space is of the second category

Let $X$ be a Baire space iff for every countable family of dense sets $\{G_n \mid n \in \Bbb N\}$ that are $G_\delta$ on $X$, we have that $\bigcap \{G_n \mid n \in \Bbb N\}$ is a dense subset of $X$.


# Locally Compact $T_2$ spaces

Every locally compact $T_2$ space is Baire space.

## Consequences in $\Bbb R$ 

We have that the set $\Bbb Q$ is not a $G_\delta$ subset on the metric of $\Bbb R$

**Th:** Let $$D_+ := \{f\in \mathcal C[0, 1] \mid \exists x \in [0, 1) (|\partial_+f(x)| < \infty)\}.$$Then $D_+$ is of first category in $\mathcal C[0, 1]$.

**Cor:** Let $D := \{f\in \mathcal C[0,1] \mid \exists x\in (0, 1) (|f'(x)| <\infty)\}$. Then $D$ is of first category.

**Cor:** The collection of all members of $\mathcal C[0, 1]$ that are not differentiable anywhere on $(0, 1)$ is of the second category in $\mathcal C[0, 1]$.

**Th:** No Banach space has a countably infinite vector space basis. 

