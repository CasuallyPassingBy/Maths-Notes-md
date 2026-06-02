---
tags:
  - MeasureTheory
  - Topology
  - GroupTheory
---
Subjects: [[Topology]], [[Measure Theory]], [[Group Theory]]
Links: [[Local Compactness]], [[Topological Groups]], [[Measures on Hausdorff Spaces]], [[Space of Continuous Compactly Supported Functions]]

**Def:** Let $G$ be a locally compact group, and let $\mu$ be a nonzero regular Borel measure on $G$. Then $\mu$ is a *left Haar measure*, or simply a *Haar measure* if it is *invariant under left translations*, or simply *translation invariant*, in the sense that $\mu(xA) = \mu(A)$ holds for each $x\in G$ and each $A\in \mathcal B(G)$. Likewise, $\mu$ is a *right Haar measure* if $\mu(Ax) = \mu(A)$ holds for each $x\in G$ and each $A\in \mathcal B(G)$. 

**Def:** Let $G$ be a group, let $x\in G$, and let $f$ be a function on $G$. The *left translate of $f$ by $x$*, written $_xf$, is defined by $_x f(t) := f(x^{-1}t)$, and the *right translate of $f$ by $x$*, written $f_x$, is defined by $f_x(t) := f(tx^{-1})$. The function $\check f$ is defined by $\check f(t) := f(t^{-1})$.

**Obs:** Let $f$ be a function on $G$, and $x, y\in G$, then $_{xy}f =\,_x(_yf)$, and $f_{xy} = (f_x)_y$. If $A$ is a subset of $G$, then the characteristic functions of the sets $A$, $xA$, and $Ax$ are related by $$(\chi_A)_x = \chi_{Ax}\quad \text{and}\quad  _x (\chi_A) = \chi_{xA}. $$
**Obs:** If $G$ is a locally compact and if $\mu$ is a left Haar measure on $G$, then  $$\int \,_xf\, d\mu = \int f\, d\mu $$holds for each Borel function $f$ that is either nonnegative or $\mu$-integrable. 

**Th:** Let $G$ be a locally compact group. Then there is a left Haar measure on $G$.

**Lemma:** Let $G$ be a locally compact group, and let $\mu$ be a left Haar measure on $G$. Then each nonempty subset $U$ of $G$ satisfies $\mu(U)>0$, and each nonnegative $f$ that belong to $\mathcal C_c(G)$ and is not identically zero satisfies $$\int f\, d\mu > 0.$$
**Th:** Let $G$ be a locally compact group, and let $\mu$ and $\nu$ be left Haar measures on $G$. Then there is a positive real number $c$ such that $\nu = c\mu$.