---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Finite Product of Measures]], [[Local Compactness]], [[Hausdorff Spaces]], [[Measures on Hausdorff Spaces]], [[Product of σ-Algebras]], [[Separable, First and Second Countable Spaces]], [[Space of Continuous Compactly Supported Functions]], [[Bourbaki's Version of Radon Measure]]

We have a couple of problems when extending the product of measure that aren't $\sigma$-finite. Let $X$ and $Y$ are locally compact Hausdorff. Then $X\times Y$ is a locally compact Hausdorff space, and it would be nice if for each pair of regular Borle measures on $X$ and $Y$, we could have a regular Borel measure on $X\times Y$. We run into two problems: regular measures can fail to be $\sigma$-finite, and the $\sigma$-algebra $\mathcal B(X)\otimes \mathcal B(Y)$ can fail to contain all the Borel subsets of $X$ and $Y$, in which case no measure on $\mathcal B(X) \otimes \mathcal B(Y)$ can be regular.

With these in mind, we will explore first the case where $X$ and $Y$ are second countable. Then we will turn to a theory of product that is suitable for Borel measure on arbitrary locally compact Hausdorff spaces. 

**Def:** Let us introduce some terminology and notation. Suppose that $X$ and $Y$ are sets and $E\subseteq X\times Y$. Then for each $x\in X$ and $y\in Y$ the *sections* $E_x$ and $E^y$ are the subsets of $Y$ and $X$ given by  $$E_x := \{y\in Y\mid (x,y)\in E\} \quad \text{and} \quad E^y := \{x\in X\mid (x, y)\in E\}. $$If $f$ is a function on $X \times Y$, then the *sections* $f_x$ and $f^y$ are functions on $Y$ and $X$ given by $$f_x(y) := f(x, y) \quad \text{and} \quad f^y(x) := f(x, y). $$

**Lemma:** Let $X$ and $Y$ be Hausdorff topological spaces, and $X\times Y$ be their product. Then
- the product $\sigma$-algebra $\mathcal B(X) \otimes \mathcal B(Y)$  is included in $\mathcal B(X\times Y)$,
- If $E\in \mathcal B(X \times Y)$, then for each $x\in X$ the section $E_x$ belongs to $\mathcal B(Y)$, and for $y\in Y$ the section $E^y$ belongs to $\mathcal B(X)$, and
- if $f:X\times Y\to \Bbb R$ is Borel measurable, then for each $x\in X$ the section $f_x:Y\to \Bbb R$ is Borel measurable, and for each $y\in Y$ the section $f^y:X \to\Bbb R$ is Borel measurable.

**Prop:** Let $X$ and $Y$ be second countable spaces. Then $\mathcal B(X\times Y) = \mathcal B(X) \times \mathcal B(Y)$. 

**Prop:** Let $X$ and $Y$ be second countable locally compact Hausdorff spaces. If $\mu$ and $\nu$ are regular Borel measures on $X$ and $Y$, respectively, then $\mu$ and $\nu$ are $\sigma$-finite, and $\mu\times \nu$ is a regular Borel measure on $X\times Y$. 

Now let us consider $X$ and $Y$ be arbitrarily compact Hausdorff spaces, and let $\mu$ and $\nu$ be regular Borel measures on $X$ and $Y$, respectively. We are gonna side step our problems where $\mu$ and $\nu$ can fail to be $\sigma$-finite and $\mathcal B(X) \otimes \mathcal B(Y) \subsetneq \mathcal B(X\times Y)$. By using Riesz representation theorem. 

**Lemma:** Suppose that $S$ and $T$ be topological spaces, that $T$ is compact, and that $f: S\times T \to \Bbb R$ is continuous. Then for each $s_0\in S$ and each $\varepsilon>0$ there is an open neighbourhood $U$ of $s_0$ such that $|f(s, t)- f(s_0, t)|<\varepsilon$ holds for each $s\in U$ and each $t\in T$. 

**Prop:** Let $X$ and $Y$ be locally compact Hausdorff spaces, and let $\mu$ and $\nu$ be regular Borel measures on $X$ and $Y$, respectively, and let $f$ belong to $\mathcal C_c(X\times Y)$. Then 
- for each $x\in X$ and $y\in Y$ the sections $f_x$ and $f^y$ belong to $\mathcal C_c(Y)$ and $\mathcal C_c(X)$, respectively,
- the functions $$x \mapsto \int_Y f(x, y)\, \nu(dy) \quad \text{and}\quad y\mapsto \int_X f(x,y)\, \mu(dx) $$belong to $\mathcal C_c(X)$ and $\mathcal C_c(Y)$, respectively, and  $$\int_X\left( \int_Y f(x, y)\, \nu(dy)\right)\, \mu(dx) = \int_Y\left(\int_X f(x, y)\, \mu(dx)\right)\, \nu(dy).$$