---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Basic Cardinal Arithmetic]], [[Arithmetic of Cardinal Numbers]], [[Alephs]], [[Generalised Continuum Hypothesis]]

Let $\langle \alpha_\nu \mid \nu < \vartheta\rangle$ be a transfinite sequence of ordinal numbers of length $\vartheta$. We say that the sequence is *increasing* if $\alpha_\mu < \alpha_\nu$, whenever $\mu < \nu < \vartheta$. If $\vartheta$ is a limit ordinal number and if $\langle \alpha_\nu \mid \nu < \vartheta\rangle$ is increasing sequence of ordinals we define
$$
\alpha = \lim_{\nu \to \vartheta} \alpha_\nu = \sup\{\alpha_\nu\mid \nu < \vartheta\} 
$$
and we call $\alpha$ the *limit* of an increasing sequence. Similarly as we did for the limit of ordinals in the [[The Normal Form for Ordinals|Normal Form]]. 

An infinite cardinal $\kappa$ is called *singular* if there exists an increasing transfinite sequence $\langle \alpha_\nu \mid \nu < \vartheta\rangle$ of ordinals $\alpha_\nu < \kappa$ whose length is $\vartheta$ is a limit ordinal less than $\kappa$, and $\kappa = \lim\limits_{\nu\to \vartheta} \alpha_\nu$. An infinite cardinal that is not singular is called *regular*.

A subset $X \subseteq \kappa$ is bounded if $\sup X < \kappa$, and *unbounded* if $\sup X = \kappa$

**Th:** Let $\kappa$ be a regular cardinal 
- If $X\subseteq \kappa$ is such that $|X| < \kappa$ then $X$ is bounded. Hence every unbounded subset of $\kappa$ has cardinality $\kappa$
- If $\lambda < \kappa$ and $f:\lambda \to \kappa$, then $f[\lambda]$ is bounded

**Lemma:** An infinite cardinal $\kappa$ is singular iff it is the sum of less than $\kappa$ smaller cardinals: $$ \kappa = \sum_{i \in I}\kappa_i$$ where $|I| <\kappa$ and $\kappa_i <\kappa$ for all $i \in I$. 

# Weak Limit Cardinals

An infinite cardinal $\aleph_\alpha$ is called a *successor cardinal*  if its index $\alpha$ is a successor ordinal. i.e., if $\aleph_\alpha = \aleph_{\beta +1}$ for some $\beta$. If $\kappa = \aleph_\beta$, then we call $\aleph_{\beta+1}$ the successor of $\kappa$ and denote it as $\kappa⁺$. If $\alpha$ is a limit ordinal, then $\aleph_\alpha$ is called a *limit cardinal*. If $\alpha >0$ is a limit ordinal, then $\aleph_\alpha$ is the limit of the sequence $\langle \aleph_\beta \mid \beta < \alpha\rangle$.

This limit cardinals, are usually called *weak limit cardinals*. 

Every successor cardinal $\aleph_{\alpha +1}$ is a regular cardinal

There are arbitrarily large singular cardinals

Suppose that $\aleph_\alpha$ is a an uncountable regular limit cardinal. Since $\alpha$ is a limit ordinal, we have $$\aleph_\alpha = \lim_{\beta \to \alpha}\aleph_\beta$$
$\aleph_\alpha$ is the limit of an increasing sequence of length $\alpha$. Since $\aleph_\alpha$ is regular then, $\alpha \ge \aleph_\alpha$, and we get that
$$ \alpha = \aleph_\alpha$$

**Lemma:** There are arbitrarily large singular cardinals $\aleph_\alpha$ such that $\aleph_\alpha = \alpha$. 

An uncountable cardinal that is both a limit cardinal and regular is called *inaccessible* (it is often called weakly inaccessible). It is impossible to prove that inaccessible cardinals exists only using ZFC. 

The property above explicitly tells us that if $\aleph_\alpha$ is a weakly inaccessible cardinal, then it is a fixed point of the [[Alephs#^a30e0d|omega function]] 

If $\alpha$ is a limit ordinal, then the *cofinality* of $\alpha$, $\text{cf}(\alpha)$, is the least ordinal number $\vartheta$ such that $\alpha$ is the limit of an increasing sequence of ordinals of length $\vartheta$. 

We see that $\text{cf}(\alpha)$ is a limit ordinal and $\text{cf}(\alpha)\le \alpha$. Thus $\aleph_\alpha$ is singular if $\text{cf}(\omega_\alpha) < \omega_\alpha$, and it is regular if $\text{cf}(\omega_\alpha) = \omega_\alpha$

We can also see that $\text{cf}(\alpha)$ is an initial ordinal. We can see that $\text{cf}(\alpha)$ is a cardinal.

**Lemma:** If a limit ordinal $\alpha$ is not a cardinal, then $\text{cf}(\alpha) < \alpha$

**Th:** For every limit ordinal $\alpha$, $\text{cf}(\text{cf}(\alpha)) = \text{cf}(\alpha)$

**Cor:** For every limit ordinal $\alpha$, $\text{cf}(\alpha)$ is a regular cardinal

**Cor:** For every limit ordinal $\alpha$, we have that $\text{cf}(\alpha) = \text{cf}(\aleph_\alpha)$. 

# Strong Limit Cardinals

An infinite cardinal $\aleph_\alpha$ is a *strong limit cardinal* if $2^{\aleph_\beta} < \aleph_\alpha$ for all $\beta < \alpha$. 

We see that, every strong limit cardinal is also a weak limit cardinal. We also get the weird thing that, not necessarily every weak limit cardinal is a strong limit cardinal: if $2^{\aleph_0}$ is greater than $\aleph_\omega$, then $\aleph_\omega$ is the counter example. If we assume the [[Generalised Continuum Hypothesis]], then every weak limit cardinal is a strong limit cardinal. So we can just call them limit cardinals.

**Th:** If $\aleph_\alpha$ is a strong limit cardinal and if $\kappa$ and $\lambda$ are infinite cardinals such that $\kappa < \aleph_\alpha$ and $\lambda < \aleph_\alpha$, then $\kappa^\lambda < \aleph_\alpha$

An uncountable cardinal number $\kappa$ is *strongly inaccessible* if it is regular and a strong limit cardinal. We see that every strongly inaccessible cardinal is weakly inaccessible, and using [[Generalised Continuum Hypothesis|GCH]], we have that a cardinal is strongly inaccessible iff it is weakly inaccessible (just having inaccessible cardinals). The reason why they are called inaccessible is because it is impossible to prove that weakly or strongly inaccessible cardinals exists only using ZFC

**Th:** Let $\kappa$ be a strongly inaccessible cardinal.
- If $|X| <\kappa$, then $|\mathcal P(X)| < \kappa$
- Let $X\in S$, iff $|X| <\kappa$ and $|S|< \kappa$, then $\left|\bigcup S\right| <\kappa$
- If $|X| <\kappa$ and $f:X \to \kappa$, then $\sup f[X] <\kappa$ 

If $\aleph_\alpha$ is strongly inaccessible and $\beta < \alpha$, then $\aleph_\alpha^{\aleph_\beta} = \aleph_\alpha$. 