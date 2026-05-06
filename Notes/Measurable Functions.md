---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Measure Spaces and Measurable Spaces]], [[Rings and Algebras of Sets]]

**Prop:** Let $(X, {\cal A})$ be a measurable space, and let $A$ be a subset of $X$ that belongs to $\cal A$. For any function $f: A\to \overline{\Bbb R}$ the conditions
- for each $t\in\Bbb R$ the set $\{x\in A \mid f(x) \le t\}$ belongs to $\cal A$,
- for each $t\in\Bbb R$ the set $\{x\in A \mid f(x) < t\}$ belongs to $\cal A$,
- for each $t\in\Bbb R$ the set $\{x\in A \mid f(x) \ge t\}$ belongs to $\cal A$, and
- for each $t\in\Bbb R$ the set $\{x\in A \mid f(x) > t\}$ belongs to $\cal A$
are equivalent. 

**Def:** Let $(X, {\cal A})$ be a measurable space, and let $A\in \cal a$. A function $f: A \to \overline{\Bbb R}$ is *measurable with respect to $\cal A$* if it satisfies one, and hence all of the conditions the proposition above. A function that is measurable with respect to $\cal A$ is sometimes $\cal A$*-measurable*, or if the $\sigma$-algebra $\cal A$ is clear from the context, simply *measurable.* If $X = \Bbb R^d,$ a function that is measurable with respect to ${\cal B}(\Bbb R^d)$ is called *Borel measurable* or *Borel function*, and a function that is measurable with respect ${\cal M}_\lambda$ is called *Lebesgue measurable.*

**Examples:**
- We see that if $f:\Bbb R^d\to \Bbb R$ is continuous, then it must be Borel measurable.
- Let $I$ be a subinterval of $\Bbb R$, and let $f: I \to\Bbb R$ be non-decreasing. Then $f$ is Borel measurable.

**Obs:** Let $(X, {\cal A})$ be a measurable space, and let $B$ be a subset of $X$. Then $\chi_B$, the characteristic function of $B$, is $\cal A$-measurable iff $B\in \cal A$.

**Def:** A function is called *simple* if it has only finitely many values.

**Obs:**  Let $(X, {\cal A})$ be a measurable space, let $f: X \to \overline{\Bbb R}$ be simple, and let $\alpha_1, \dots, \alpha_n$ be the values of $f$. Then $f$ is measurable iff $\{x\in X\mid f(x) = \alpha_i\}\in \cal A$ for $i = 1,\dots, n$. 

**Prop:** Let $(X, {\cal A})$ be a measurable space, and let $A$ be a subset $X$ that belongs to $\cal A$, and let $f$ and $g$ be $\overline{\Bbb R}$ -valued measurable functions on $A$. Then the sets $\{x\in A \mid f(x) <g(x)\},$ $\{x\in A\mid f(x) \le g(x)\},$ and $\{x\in A \mid f(x) = g(x)\}$ belongs to $\cal A$.

**Def:** Let $f, g: A \to \overline{\Bbb R}$. The *maximum* and *minimum* of $f$ and $g$, written $f \lor g$ and $f\land g$, are the functions from defined by $$(f \lor g)(x) := \max\{f(x), g(x)\}, \qquad (f \land g)(x) := \min\{f(x), g(x)\}. $$
**Prop:** Let $(X, {\cal A})$ be a measurable space, and let $A$ be a subset $X$ that belongs to $\cal A$, and let $f, g:A \to \overline{\Bbb R}$ be measurable functions on $A$. Then $f\lor g$ and $f\land g$ are measurable.

**Def:** If for each $n <\omega$ there is a function $f_n: A\to \overline{\Bbb R}$, then we $$(\sup f_n)(x) := \sup\{f_n(x) \mid n<\omega\},$$and $\inf f_n$, $\limsup f_n$, $\liminf f_n$ and $\lim f_n$ are defined in analogous ways. The domain of $\lim f_n$ consists of those points in $A$ at which the limits exist. Each of this functions can have infinite values, even if all the $f_n$'s have only finite values.

**Lemma:**  Let $(X, {\cal A})$ be a measurable space, and let $\{f_n\}_{n<\omega}$ be a sequence of measurable functions on $X$. Then $\{x\in X \mid \lim f_n(x) \text{ exists and it is finite}\}$ belongs to $\cal A.$

**Prop:** Let $(X, {\cal A})$ be a measurable space, and let $A$ be a subset $X$ that belongs to $\cal A$, and let $\{f_n\}_{n<\omega}$ be a sequence of measurable functions on $A$. Then
- the functions $\sup f_n$ and $\inf f_n$ are measurable,
- the functions $\limsup f_n$ and $\liminf f_n$ are measurable, and 
- the function $\lim f_n$ is measurable. 

**Prop:** Let $(X, {\cal A})$ be a measurable space, and let $A$ be a subset $X$ that belongs to $\cal A$, let $f, g:A \to [0,\infty]$ be measurable functions on $A$, and lat $\alpha \ge 0$. Then $\alpha f$ and $f+g$ are measurable.

**Prop:** Let $(X, {\cal A})$ be a measurable space, and let $A$ be a subset $X$ that belongs to $\cal A$, let $f, g:A \to {\Bbb R}$ be measurable functions on $A$, and let $\alpha\in \Bbb R$. Then $\alpha f$, $f+g$, $f-g$, $fg$, and $f-g$, where the domain of $f/g$ is $\{x\in A\mid g(x) \neq 0\}$.

**Def:** Let $A$ be a set, and let $f$ be an extended real-valued function on $A$. The *positive part $f^+$* and the *negative part $f^-$* of $f$ are the extended real-valued functions defined on $$f^+(x) := \max\{f(x), 0\}, \qquad f^-(x) := -\min(f(x), 0). $$Thus $f^+ = f\lor 0$, and $f^- = (-f) \lor 0$. 

**Obs:** It is easy to see that if $(X,{\cal A})$ is measurable space if $f: A\to \overline{\Bbb R}$, where $A\subseteq X$, then $f$ is measurable iff $f^+$ and $f^-$ are both measurable. It follows from this remar, that the absolute value $|f|$ of a measurable function $f$ is measurable.

**Prop:** Let $(X, {\cal A})$ be a measurable space, and let $A$ be a subset of $X$ that belongs to $\cal A$, and let $f: A \to [0, \infty]$. Then there is a sequence $\{f_n: A \to \Bbb R^{\ge 0} \}_{n< \omega}$ of simple functions that satisfy $$ f_1(x) \le f_2(x) \le \cdots\le f_n(x) \le f_{n+1}(x)\le \cdots, \qquad \text{and}\qquad f(x) = \lim f_n(x)$$at each $x\in A$.

**Prop:** Let $(X, {\cal A})$ be a measurable space, and let $A$ be a subset of $X$ that belongs to $\cal A$. For a function $f:A \to \Bbb R$, the conditions
- $f$ is measurable with respect to $\cal A$,
- for each open subset $U$ of $\Bbb R$ the set $f^{-1}[U]\in \cal A$,
- for each closed subset $C$ of $\Bbb R$ the set $f^{-1}[C] \in \cal A$,
- for each Borel subset $B$ of $\Bbb R$ the set $f^{-1}[B]\in \cal A$
are equivalent.

**Prop:** there is a Lebesgue measurable subset of $\Bbb R$ that is not a Borel set.

**Prop:** Let $(X, {\cal A},\mu)$ be a measure space, and let $f, g: X \to \overline{\Bbb R}$ that are equal almost everywhere. If $\mu$ is complete and if $f$ is $\cal A$-measurable, then $g$ is $\cal A$-measurable.

**Cor:** Let $(X, {\cal A},\mu)$ be a measure space, let $\{f_n\}$ be a sequence measurable functions on $X,$ and let $f: X\to \overline{\Bbb R}$ such that $\{f_n\}$ converges to $f$ almost everywhere. If $\mu$ is complete if each $f_n$ is $\cal A$-measurable, then $f$ is $\cal A$-measurable.

**Cor:** Let $f, g: \Bbb R \to \Bbb R$ continuous functions. If $f = g$ $\lambda$-almost everywhere, then $f =g$. 

**Cor:** Let $(X, {\cal A},\mu)$ be a measure space. and let $f, f_n: X \to \overline{\Bbb R}$ be $\cal A$-measurable function for each $n <\omega$. If $\{f_n\}$ converges to $f$ almost everywhere, then there are $\cal A$-measurable functions $g_1,g_2,\dots,$ that are equal to $f_1, f_2, \dots,$ almost everywhere and satisfy $f = \lim g_n$.

**Prop:** Let $(X, {\cal A},\mu)$ be a measure space and let $\cal A_\mu$ be the completion of $\cal A$ under $\mu$. Then a function $f: X \to \overline{\Bbb R}$ is $\cal A_\mu$-measurable iff there are $\cal A$-measurable functions $f_0, f_1: X \to \overline{\Bbb R}$ such that $f_0 \le f \le f_1$ holds everywhere on $X$ and $f_0 = f_1$ holds $\mu$-almost everywhere on $X$.

# General Measurable Functions

**Def:** Let $(X, {\scr A})$ and $(Y, {\scr B})$ be measurable spaces. A function $f:X \to Y$ is *measurable with respect to $\scr A$ and $\scr B$* if for each $B\in \scr B$ the set $f^{-1}[B]$ belongs to $\scr A$. Instead of saying that $f$ is measurable with respect to $\scr A$ and $\scr B$, we will say that $f$ is a *measurable function* from $(X, {\scr A})$ to $(Y, {\scr B})$, that $f: (X, {\scr A})\to (Y, {\scr B})$ is *measurable*, or simply that $f$ is a $({\scr A,\scr B})$-measurable. Note that if the $\sigma$-algebra in the codomain is obvious we are gonna denote it as $\scr A$-measurable, or simply measurable when it is understood. 

Let $(X, {\scr A})$ and $(Y, {\scr B})$ be measurable spaces. A bijection $f:X \to Y$ is a *Borel isomorphism* or simply an *isomorphism* if $f$ is $({\scr A}, {\scr B})$-measurable and $f^{-1}$ is $({\scr B}, {\scr A})$-measurable. Equivalently, the bijection $f$ is an isomorphism if the subsets $A$ of $X$ that belong to $\scr A$ are exactly those for which $f[A]$ belongs to $\scr B$. The spaces $(X, {\scr A})$ and $(Y, {\scr B})$ are *Borel isomorphic* or *isomorphic* if there exists an isomorphism. 

This definition is completely analogous to [[Continuous Functions and Homeomorphims|continuous functions in topological spaces]]. 

**Prop:** Let $(X, {\scr A})$, $(Y, {\scr B})$, and $(Z, {\scr C})$ be measurable spaces, and let $f: (X, {\scr A}) \to (Y, {\scr B})$ and $g: (Y, {\scr B}) \to (Z, {\scr C})$ be measurable. Then $g\circ f: (X, {\scr A}) \to (Z, {\scr C})$ is measurable.

**Prop:** Let $(X, {\scr A})$ and $(Y, {\scr B})$ be measurable spaces, and let ${\scr B}_0\subseteq {\cal P}(Y)$ such that $\sigma({\scr B}_0)= \scr B$. Then a function $f:X \to Y$ is $({\scr A}, {\scr B})$-measurable iff $f^{-1}[B] \in \scr A$ holds for each $B\in {\scr B}_0$.

**Def:** Let ${\cal B}(\overline{\Bbb R})$ be the collection of all subsets of $\overline{\Bbb R}$ of the form $B\cup C$, where $B\in {\cal B}(\Bbb R)$ and $C\subseteq\{\pm\infty\}$. 

**Prop:** Let $(X, {\scr A})$ be a measurable space, and let $f: X \to \overline{\Bbb R}$ be a function. Then $f$ is ${\scr A}$-measurable in the usual sense iff it is $({\scr A}, {\cal B}(\overline{\Bbb R}))$-measurable.

**Example:** Let $(X, {\scr A})$ be a measurable space, and let $f: X \to \Bbb R^d$. If $f= (f_1,\dots, f_d)$, then $f$ is $({\scr A}, {\cal B}(\Bbb R^d))$-measurable iff $f_1, \dots, f_d$ are $\scr A$-measurable. We see that the class of measurable function from $(X, {\scr A})$ to $(\Bbb R^d, {\cal B}(\Bbb R^d ))$ is a vector space that is closed under limits.

**Obs:** If we consider the space $\Bbb R^2$, and identify it with the set $\Bbb C$ of complex numbers. We see that a function $f:X \to \Bbb C$ is $({\scr A}, {\cal B}(\Bbb C))$-measurable iff its real and imaginary parts are ${\scr A}$-measurable, and that collection of measurable functions from $(X, {\scr A})$ to $(\Bbb C,{\cal B}(\Bbb C))$ is a real vector space closed under limits. We can show that the product of two measurable complex-valued function on $X$ is measurable; thus we can extend that the space of measurable functions from $(X, {\scr A})$ to $(\Bbb C,{\cal B}(\Bbb C))$ is a complex vector space closed under limits.

**Prop:** Let $(X, {\scr A})$ be a measurable space, and let $f, g:X \to \Bbb C$ be measurable. If $g$ does not vanish, then $f/g$ is measurable. 

In the special case where we consider topological spaces $(X, \tau_1)$ and $(Y, \tau_2)$, we naturally consider their Borel $\sigma$-algebra generated by their topology. If a function $f:X \to Y$ is measurable with respects to these $\sigma$-algebras, then it is called in particular *Borel measurable*. 

**Prop:** Let $f:X \to Y$ be a continuous functions between topological spaces, then $f$ is Borel measurable.

**Lemma:** Let $(X, {\scr A})$ be a measurable space, and let $Y$ be a metrizable topological space. Then a function $f:X \to Y$ is measurable with respect to $\scr A$ and $\mathcal B(Y)$ iff for each continuous function $g: Y\to\Bbb R$ the function $g\circ f$ is $\scr A$-measurable. 

## Image Measures

**Def:** Let $(X, {\scr A},\mu)$ be a measure space, let $(Y, {\scr B})$ be a measurable space and let $f: X\to Y$ be measurable. We define a a function $\mu f^{-1}: {\scr B}\to [0,\infty]$ by letting $\mu f^{-1}(B) = \mu(f^{-1}[B])$ for each $B\in \scr B$. We see that $\mu f^{-1}$ is a measure on $(Y, {\scr B})$. The measure $\mu f^{-1}$ is sometimes called the *image of $\mu$ under $f$.* Another notation for $\mu f^{-1}$ is $\mu \circ f^{-1}$.

**Prop:** Let $(X, {\scr A},\mu)$ be a measure space, let $(Y, {\scr B})$ be a measurable space and let $f: X\to Y$ be measurable. Let $g: Y\to \overline{\Bbb R}$ be a $\scr B$-measurable function. Then $g$ is $\mu f^{-1}$ integrable iff $g\circ f$ is $\mu$-integrable. If these functions are integrable, then $$\int_Y g \ d(\mu f^{-1}) = \int_X (g\circ f)\, d\mu. $$
