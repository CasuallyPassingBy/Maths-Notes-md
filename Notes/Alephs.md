---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Ordinal Numbers]]

**Def:** An ordinal number $\alpha$ is called an **initial ordinal** if it is not equipontent to any $\beta < \alpha$

********Th:******** Each well-orderable set $X$ is equipotent to a unique initial ordinal number

**Def:** For any set $A$, let $h(A)$ be the least ordinal number which is not equipotent to any subset if $A$. $h(A)$ is called the **Hartog's number** of $A$. By definition $h(A)$ is the least ordinal $\alpha$ such that ${|\alpha|\not\le |A|}$

**************Lemma:************** For any $A$, $h(A)$ is an initial ordinal number

**************Lemma:************** The Hartog's number of $A$ exists for all $A$

**Def:**
- $\omega_0 = \omega$
- $\omega_{\alpha +1} = h(\omega_\alpha)$ for all $\alpha$
- $\omega_\alpha = \sup \{\omega_\beta\mid \beta < \alpha\}$ for all limit ordinal $\alpha \ne 0$ ^a30e0d

From this we see that for any ordinal $\alpha$, $\alpha \le \omega_\alpha$ 

********Th:********
- $\omega_\alpha$ is an infinite initial ordinal for each $\alpha$
- If $\Omega$ is an infinite initial ordinal, then $\Omega = \omega_\alpha$ for some $\alpha$

The conclusion of this section is that every well-orderable set is equipotent to a unique initial ordinal number and that that infinite initial ordinal numbers form a transfinite sequence $\omega_\alpha$ with $\alpha$ ranging over all ordinal numbers. Infinite initial ordinals are, by definition, the cardinalities of infinite well-orderable sets. It is customary to call these cardinal numbers _**alephs**_, thus we define

$$ \aleph_\alpha =|\omega_\alpha| $$

# Additions and Multiplication of Alephs

********Th: $\aleph_\alpha\cdot \aleph_\alpha = \aleph_\alpha$** for every $\alpha$

**Cor:** For every $\alpha$ and $\beta$ such that $\alpha \le \beta$ we have that

$$ \aleph_\alpha \cdot \aleph_\beta = \aleph_\beta $$

also

$$ n \cdot \aleph_\beta = \aleph_\alpha $$

**Cor:** For every $\alpha$ and $\beta$ such that $\alpha \le \beta$ we have that

$$ \aleph_\alpha+\aleph_\beta = \aleph_\beta $$

also

$$ n + \aleph_\alpha = \aleph_\alpha $$

**********Cor:********** For all $n \in \omega$ and $n >0$

- $\aleph_\alpha^n = \aleph_\alpha$
- $|[\omega_\alpha]^n| = \aleph_\alpha$, where $[\omega_\alpha]^n$ is the set of $n$ element subsets of $\omega_\alpha$.
- $|[ \omega_\alpha]^{< \omega} | = \aleph_\alpha$, where $[\omega_\alpha]^{<\omega} = \bigcup_{n < \omega} [\omega_\alpha]^n$, or the set of all finite subsets of $\omega_\alpha$

**************Cor:************** If $\alpha$ and $\beta$ are ordinals such that $|\alpha| , |\beta | \le \aleph_\gamma$, then $|\alpha+\beta|, |\alpha\cdot\beta|, |\alpha^\beta| \le \aleph_\gamma$

**Cor:** Let $f$ be a function with domain $\omega_\alpha$, then $|\operatorname{Im} f| \le \aleph_\alpha$

**Cor:** If $X$ is a subset of $\omega_\alpha$ such that $|X| < \aleph_ \alpha$, then $|\omega_\alpha -X | = \aleph_ \alpha$