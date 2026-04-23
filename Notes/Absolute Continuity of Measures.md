---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Measures]], [[Signed and Complex Measures]], [[Scalar Integral on Measure Spaces]]

**Def:** Let $(X, {\scr A})$ be a measurable space, and let $\mu$ and $\nu$ be positive measures on $(X, {\scr A})$. Then $\nu$ is *absolutely continuous with respect to $\mu$* if for each set $A\in \scr A$ that satisfy $\mu(A) = 0$ implies $\nu(A) = 0$. One sometimes write $\nu \ll \mu$ to indicate that $\nu$ is absolutely continuous with respect to $\mu$. A measure on $(\Bbb R^d, \mathcal B(\Bbb R^d ))$ is simply called *absolutely continuous* if it is absolutely continuous with respect to $d$-dimensional Lebesgue measure.

**Obs:** If we only consider positive measures, then being absolutely continuous with respect to another measure is a transitive relation. 

**Obs:** Suppose that $(X, {\scr A},\Bbb R)$ is a measure space and let $f$ be a nonnegative function in ${\scr L}^1(X, {\scr A},\mu, \Bbb R)$. We see that the measure $\nu(A) := \int_A f\, d\mu$ is absolutely continuous with respect to $\mu$, since if $\mu(A) = 0$, then $f\chi_A$ is zero $\mu$-almost everywhere and $\nu(A) = 0$.

**Lemma:** Let $(X, {\scr A})$ be a measurable space, and let $\mu$ be a positive measure on $(X, {\scr A})$, and let $\nu$ be a finite positive measure on $(X, {\scr A})$. Then $\nu \ll \mu$ iff for each positive $\varepsilon$ there is a positive $\delta$ such that for each $A\in \scr A$ that satisfies $\mu(A)<\delta$ also satisfies $\nu(A) <\varepsilon$. 

**Radon-Nidkodym Theorem:** Let $(X, {\scr A})$ be a measurable space, let $\mu$ be a $\sigma$-finite measure on $(X, {\scr A})$ and let $\nu$ be a measure on $(X, {\scr A})$. If $\nu$ is absolutely continuous with respect to $\mu$, then there is an $\scr A$-measurable function $g: X\to [0,\infty]$ such that $$\nu(A) = \int_A g\,d\mu$$holds for each $A\in \scr A$. The function $g$ is unique up to $\mu$-almost everywhere equality. If in addition, $\nu$ is $\sigma$-finite, then we know that $g: X \to [0,\infty)$.

**Def:** Suppose $(X, {\scr A})$ is a measurable space, that $\mu$ is a positive measure on $(X, {\scr A})$, and that $\nu$ is a signed or complex measure on $(X, {\scr A})$. Then $\nu$ is *absolutely continuous respect to $\mu$*, written $\nu\ll\mu$, if its variation $|\nu|$ is absolutely continuous with respect to $\mu$. 

**Obs:** It is easy to see that a signed measure $\nu$ is absolutely continuous with respect to $\mu$ iff $\nu^+$ and $\nu^-$ are absolutely continuous with respect to $\mu$, and that a complex measure $\nu$ is absolutely continuous with respect to $\mu$ iff the measure $\nu_1, \nu_2, \nu_3$ and $\nu_4$ appearing in its Jordan decomposition $\nu = (\nu_1-\nu_2)+i(\nu_3-\nu_4)$ are absolutely continuous with respect to $\mu$. It is also easy to check that a signed or complex measure $\nu$ is absolutely continuous with respect to $\mu$ iff for each $A\in \scr A$ that satisfies $\mu(A) = 0$ also satisfies $\nu(A) = 0$. 

**Radon-Nidkodym Theorem for Signed and Complex Measures:** Let $(X, {\scr A})$ be a measurable space, and let $\mu$ be a $\sigma$-finite measure on $(X, {\scr A})$, and let $\nu$ be a finite signed or complex measure on $(X, {\scr A})$. If $\nu$ is absolutely continuous with respect to $\mu$, then there is a function $g\in {\scr L}^1(X, {\scr A}, \mu)$ and satisfies$$\nu(A) = \int_A g\, d\mu $$for each $A\in \scr A$. The function $g$ is unique up to $\mu$-almost everywhere equality.

**Def:** Let $(X, {\scr A})$ be a measurable space, and let $\mu$ be a $\sigma$-finite positive measure on $(X, {\scr A})$, and let $\nu$ be a finite, signed, complex, of $\sigma$-finite measure on $(X, {\scr A})$. Suppose that $\nu$ is absolutely continuous with respect to $\mu$. An $\scr A$-measurable function $g$ that satisfies $\nu(A) = \int_A g\, d\mu$ for each $A\in \scr A$ is called a *Radon-Nikodym derivative* of $\nu$ with respect to $\mu$ or, in view of its uniqueness up to $\mu$-null sets, *the Radon Nikodym derivative*  of $\nu$ with respect to $\mu$. A Radon-Nikodym derivative of $\nu$ with respect to $\mu$ is sometimes denoted by $$\frac{d \nu}{d\mu}.  $$ ^22e27b

**Prop:** Suppose $\mu$ is a $\sigma$-finite positive measures on $(X, {\scr A})$, $\nu$ is a measure on $(X, {\scr A})$, and that $\nu\ll\mu$. Then an $\scr A$-measurable function $f:X \to \Bbb R$ is $\nu$-integrable iff $f\dfrac{d\nu}{d\mu}$ is $\mu$-integrable. Additionally, if those functions are integrable, then $$\int f\, d\nu = \int f\frac{d\nu}{d\mu} \, d\mu. $$
**Prop:** Suppose $\nu_1, \nu_2$ and $\nu_3$ are $\sigma$-finite positive measures on $(X, {\scr A})$, that $\nu_1 \ll\nu_2$ and $\nu_2\ll\nu_3$. Then $\nu_1 \ll \nu_3$, and $$\frac{d\nu_1}{d\nu_3} =\frac{d\nu_1}{d\nu_2}\frac{d\nu_2}{d\nu_3}  $$
**Prop:** Let $\mu$ and $\nu$ be $\sigma$-finite positive measures on $(X, {\scr A})$. The following statements are equivalent. ^2315d6
- $\nu\ll\mu$ and $\mu\ll\nu$.
- $\mu$ and $\nu$ have exactly the same sets of measure zero.
- there is an $\scr A$-measurable function $g:X \to (0,\infty)$ such that $$\nu(A) = \int_A g\, d\mu  $$holds for each $A\in \scr A$.

**Cor:** Let $\mu$ and $\nu$ be $\sigma$-finite positive measures on $(X, {\scr A})$. If $\nu\ll\mu$ and $\mu\ll\nu$, then $\dfrac{d\mu}{d\nu}$ and $\dfrac{d\nu}{d\mu}$ both exists, are positive, and are related by $$\dfrac{d\mu}{d\nu} = \left(\dfrac{d\nu}{d\mu}\right)^{-1}.$$
**Cor:** If $\mu$ is a $\sigma$-finite measure on $(X, {\scr A})$, then there is a finite measure $\nu$ on $(X, {\scr A})$ such that $\nu \ll \mu$ and $\mu \ll \nu$.

**Prop:** Suppose $(X, {\scr A},\mu)$ is a measure space, and let $f\in {\scr L}^1(X, {\scr A}, \mu, \Bbb R)$ or $f\in {\scr L}^1(X, {\scr A}, \mu, \Bbb C)$, and $\nu$ is the finite signed measure or complex measure defined by $\nu(A) := \int_A f\, d\mu$. Then $$|\nu| (A) = \int_A |f|\, d\mu $$holds for each $A\in \scr A$.

**Cor:** Let $\nu$ be a finite signed or complex measure on the measurable space $(X, {\scr A})$. Then the Radon-Nikodym derivative of $\nu$ with respect to $|\nu|$ has absolute value $1$ at $|\nu|$-almost every point in $X$, meaning that  $$\left|\frac{d\nu}{d|\nu|}\right| = 1 \quad \text{a.e.}[|\nu|].$$
**Cor:** Let $(X, {\scr A})$ be a measurable space, let $\mu$ be a finite signed or complex measure on $(X,{\scr A})$, and let $f$ be a bounded real or complex-valued $\scr A$-measurbale function on $X$. Then  $$\left|\int f\, d\mu\right|\le \int |f|\, d|\mu|. $$
**Prop:** Let $\mu$ be a $\sigma$-finite positive measure on $(X, {\scr A})$. We see that $$M_\mu :=\{\nu\in M(X, {\scr A}, \Bbb R) \mid \nu \ll\mu\}$$ is a closed linear subspace of the normed linear space $M(X, {\scr A},\Bbb R)$. There is a [[Isometries on Metric Spaces|isometric]] isomorphism from $M_\mu$ onto $L^1(X, {\scr A},\mu)$.

# Singularity

**Def:** Let $(X, {\scr A})$ be a measurable space. A positive measure $\mu$ on $(X, {\scr A})$ is *concentrated* on the $\scr A$-measurable set $E$ if $\mu(X\setminus E) = 0$. A signed or complex measure $\mu$ on $(X,{\scr A})$ is *concentrated* on $E\in \scr A$ if the variation $|\mu|$ of $\mu$ is concentrated on $E$. Now suppose $\mu$ and $\nu$ are positive, signed, or complex measures on $(X,{\scr A})$. Then $\mu$ and $\nu$ are *mutually singular* if there is an $E\in\scr A$ such that $\mu$ is concentrated on $E$ and $\nu$ is concentrated on $X\setminus E$. One sometimes writes $\mu \perp \nu$ to indicate that $\mu$ and $\nu$ are mutually singular. Instead of saying that $\mu$ and $\nu$ are mutually singular, one sometimes says that $\mu$ and $\nu$ are singular, that $\nu$ is singular with respect to $\mu$, or that $\mu$ is singular with respect to $\nu$. A positive, signed or complex measure on $(\Bbb R^d, {\cal B}(\Bbb R^d))$ is simply called *singular* if it is singular with respect to the $d$-dimensional Lebesgue measure.

**Prop:** Let $\mu$ be a positive measure on $(X, {\scr A})$, and let $\nu$ be a positive, signed or complex measure on $(X, {\scr A})$. If $\nu \ll \mu$ and $\nu \perp \mu$, then $\nu = 0$. 

**Prop:** Let $\mu$ be a positive measure on $(X, {\scr A})$, and let $\nu$ be a positive, signed or complex measure on $(X, {\scr A})$. Then  $$\{\nu \in M(X, {\scr A},\Bbb R) \mid \nu \perp \mu\}$$is a closed linear subspace of the normed space $M(X, {\scr A},\Bbb R)$. 

**Lebesgue Decomposition Theorem:** Let $(X, {\scr A})$ be a measurable space, and let $\mu$ be a positive measure on $(X, {\scr A})$, and let $\nu$ be a finite signed complex, or $\sigma$-finite positive measure on $(X, {\scr A})$. Then are unique finite signed, complex or positive measures $\nu_a$ and $\nu_s$ on $(X, {\scr A})$ such that
- $\nu_a$ is absolutely continuous with respect to $\mu$,
- $\nu_s$ is singular with respect to $\mu$, and 
- $\nu = \nu_a+\nu_s$.

The decomposition $\nu = \nu_a +\nu_s$ is called the *Lebesgue decomposition* of $\nu$, while $\nu_a$ and $\nu_s$ are called *absolutely continuous* and *singular parts* of $\nu$. 

**Prop:** Let $\mu$ be a positive measure on $(X, {\scr A})$, and let $\nu$ be a positive, signed or complex measure on $(X, {\scr A})$, and let $\nu = \nu_a + \nu_s$ be the Lebesgue decomposition of $\nu$. Then $\|\nu\| = \|\nu_a\| + \|\nu_s\|$. 

**Prop:** Let $\mu$ and $\nu$ be positive measures on $(X, {\scr A})$ such that for each $\varepsilon> 0$ there is a set $A\in \scr A$ such that $\mu(A)<\varepsilon$ and $\nu(X\setminus A) <\varepsilon$. Then $\mu \perp \nu$.

**Prop:** Let $\mu$ and $\nu$ be positive measures on $(X, {\scr A})$. The following statements are equivalent.
- $\mu \perp \nu$.
- $\mu \vee \nu = 0$.
- $\mu \vee \nu = m+\nu$.