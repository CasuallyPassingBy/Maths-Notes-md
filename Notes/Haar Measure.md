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

**Prop:** Let $G$ be a locally compact group, let $\mu$ be a left Haar measure on $G$, and let $f$ and $g$ be continuous complex valued functions on $G$. If $f$ and $g$ are equal $\mu$-almost everywhere, then they are equal everywhere. 

**Prop:** Let $G$ be a locally compact group, and let $\mu$ be a left Haar measure on $G$. The topology on $G$ is discrete iff $\mu(\{x\}) \ne  0$ holds for some $x\in G$. 

Let $G$ be a locally compact group, and let $\mu$ be a regular Borel measure on $G$. The map $x\mapsto x^{-1}$ is a homeomorphism of $G$ onto itself, and so the subsets of $A$ and $G$ that belong to $\mathcal B(G)$ are exactly those for which $A^{-1}$ belongs to $\mathcal B(G)$. Define a function $\check\mu$ on $\mathcal B(G)$ by $\check \mu(A) := \mu(A^{-1})$. We see that  $$\int f\, d\check\mu = \int \check f\, d\mu $$holds if $f$ is a Borel function that is nonnegative or $\check\mu$-integrable.

**Prop:** Let $G$ be a locally compact group, and let $\mu$ be a regular Borel measure on $G$. Then $\mu$ is a left Haar measure iff $\check\mu$ is a right Haar measure, and is a right Haar measure iff $\check\mu$ is a left Haar measure.

**Cor:** Let $G$ be a locally compact group. Then there is one and, up to a constant multiple, only one right measure on $G$.

**Prop:** Let $G$ be a locally compact group, and let $\mu$ be a left Haar measure on $G$. Then $\mu$ is finite iff $G$ is compact.

For a compact group $G$, we typically scale $\mu$ such that $\mu(G) = 1$ (normalised Haar measure)

**Def:** Let $G$ be a locally compact group, and let $\mu$ be a left Haar measure on $G$. The maps $u\mapsto ux$ are homeomorphism of $G$ onto itself, and so for each $x\in G$ the formula $\mu_x(A) = \mu(Ax)$ defines a regular Borel measure $\mu_x$ on $G$. The translation invariance of $\mu$ implies that $\mu_x$ satisfies $\mu_x(yA) = \mu(yAx) = \mu(Ax) = \mu_x(A)$ for each $y\in G$ and $A\in \mathcal B(G)$. Thus $\mu_x$ is a left Haar measure, and so we see that for each $x$ there is a positive number, say $\Delta(x)$, such that $\mu_x= \Delta(x) \mu$. The function $\Delta:G \to \Bbb R$ defined in this way is called the *modular function* of $G$. 

If $\nu$ is another left Haar measure on $G$, then there is a positive constant $c$ such that $\nu = c\mu$, and so $\nu_x = c\mu_x = c\Delta(x) \mu = \Delta(x) \nu$ holds for each $x\in G$. Thus the modular function $\Delta$ is determined by the group $G$ and does depend on the particular left Haar measure used in its definition. 

We see that  $$\int f_x\, d\mu = \Delta(x) \int f\,d\mu $$holds if $f$ is the characteristic function of a Borel subset of $G$ and hence if $f$ is a Borel function that is nonnegative or $\mu$-integrable.

**Prop:** Let $G$ be a locally compact group, and let $\Delta$ be the modular function of $G$. Then $\Delta:G \to \Bbb R^\times$ is a continuous group homomorphism.

**Prop:** Let $G$ be a locally compact group, and let $\mu$ be a right Haar measure on $G$. Then $\mu(xA) = \Delta(x^{-1})\mu(A)$ holds for each $x\in G$ and each $A\in\mathcal B(G)$. 

**Def:** A locally compact group $G$ is *unimodular* if its modular function satisfies $\Delta(x) = 1$ at each $x\in G$.

**Obs:** Thus a locally compact group $G$ is unimodular iff each left Haar measure on $G$ is a right Haar measure and so iff the collection of measures on $G$ coincide with the collection of all right Haar measures on $G$. We see that every commutative locally compact group is unimodular.

**Prop:** Every compact group is unimodular.

**Prop:** Let $G$ be a locally compact group, and let $\mu$ be a left Haar measure on $G$. Then each Borel subset $A$ of $G$ satisfies $$\check\mu (A) =\int_A \Delta(x^{-1}) \, d\mu. $$We see that  $$\frac{d \check \mu}{d\mu}(x) = \Delta(x^{-1})=\check\Delta(x) \qquad\text{and}\qquad \frac{d\mu}{d\check\mu}(x) = \Delta(x)$$
**Cor:** Let $G$ be a locally compact group, let $\mu$ be a left Haar measure on $G$, and let $\nu$ be a right Haar measure on $G$. Then a Borel subset satisfies $\mu(A)= 0$ iff it satisfies $\nu(A) = 0$

**Cor:** Let $G$ be a locally compact group, and let $\mu$ be a left Haar measure on $G$. Then $G$ is unimodular iff $\mu = \check\mu$. 

**Prop:** Let $G$ be a locally compact group, and let $\mu$ be a left Haar measure on $G$. Then $\mu$ is $\sigma$-finite iff $G$ is $\sigma$-compact.

**Prop:** Let $G$ be a locally compact group, let $\mu$ be a left Haar measure on $G$, and let $\nu$ be a right Haar measure on $G$. Suppose the outer measure $\mu^*$ and $\nu^*$ induced by $\mu$ and $\nu$, respectively, and $\mu_1$ and $\nu_1$ be the restriction of $\mu^*$ and $\nu^*$ to their measurable sets.
- Let $A\subseteq X$. $A$ is $\mu$-measurable iff it is $\nu$-measurable.
- A subset of $G$ is locally $\mu_1$-null iff it is locally $\nu_1$-null. 