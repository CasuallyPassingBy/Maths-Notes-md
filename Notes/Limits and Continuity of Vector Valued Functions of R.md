---
tags:
  - VectorAnalysis
  - DifferentialGeometry
---
Subjects: [[Vector Analysis]]
Links: [[Vector-valued functions of R]], [[Connected Sets in Rn#Path-Connected Sets|Path Connected Sets]], [[Topological Characterization of Continuity in Rn]]

**Def:** Let $f: D\subseteq \Bbb R\to\Bbb R^n$, and let $a$ be cluster point of $D$, and $q \in\Bbb R^n$. Then we can write that $\lim_{t\to a}f(t) =q$ if any sequence $(a_k) \to a$, and $a_k \Bbb Ne a$ for all $k\in \Bbb N$, then $f(a_k) \to L$.

********Th:******** Let $f: D\subseteq \Bbb R\to\Bbb R^n$, and $a$ a cluster point of $D$, then $\lim_{x\to a}f(x) = L$, iff for all ${1 \le i \le n}$, $\lim_{x\to a}f_i(x) = q_i$ in $\Bbb R$.

********Th:******** Let $f: D\subseteq \Bbb R\to\Bbb R^n$, and $a$ a cluster point of $D$, then $\lim_{x\to a}f(x) = L$ iff:

$$ \forall\varepsilon >0\exists>0\forall x\in D[0<|x-a|<\delta \implies \|f(x) - L\| < \varepsilon] $$

### One Sided Limits
**Def:** Let $f: D\subseteq \Bbb R\to\Bbb R^n$, and let $a$ be a point of $D$, and $q \in\Bbb R^n$. Then we can write that $\lim_{t\to a^+}f(t) =\mathbf{q}$ if any sequence $(a_k) \to a$, and $a_k > a$ for all $k\in \Bbb N$, then ${f(a_k) \to L^+}$.

********Th:******** Let $f: D\subseteq \Bbb R\to\Bbb R^n$, and$a$ be a point of $D$, then $\lim_{x\to a^+}f(x) = \mathbf{q}$, iff for all ${1 \le i \le n}$, $\lim_{x\to a^+}f_i(x) = L^+_i$ in $\Bbb R$.

********Th:******** Let $f: D\subseteq \Bbb R\to\Bbb R^n$, and $a$ be a point of $D$, then $\lim_{x\to a^+}f(x) = L^-$ iff:

$$ \forall\varepsilon >0\exists>0\forall x\in D[0<x-a <\delta \implies \|f(x) - L^-| < \varepsilon] $$

**Def:** Let $f: D\subseteq \Bbb R\to\Bbb R^n$, and let $a$ be left cluster point of $D$, and $q \in\Bbb R^n$. Then we can write that $\lim_{t\to a^-}f(t) =L^-$ if any sequence $(a_k) \to a$, and $a_k < a$ for all $k\in \Bbb N$, then $f(a_k) \to L^-$.

********Th:******** Let $f: D\subseteq \Bbb R\to\Bbb R^n$, and$a$ be a point of $D$, then $\lim_{x\to a^-}f(x) = \mathbf{q}$, iff for all ${1 \le i \le n}$, $\lim_{x\to a^-}f_i(x) = q_i$ in $\Bbb R$.

********Th:******** Let $f: D\subseteq \Bbb R\to\Bbb R^n$, and $a$ a cluster point of $D$, then $\lim_{x\to a^+}f(x) = L^+$ iff:

$$ \forall\varepsilon >0\exists>0\forall x\in D[0<a-x <\delta \implies \|f(x) - L^+\| < \varepsilon] $$

********Th:******** Let $f: D\subseteq \Bbb R\to\Bbb R^n$, and $a$ a cluster point of $D$, then $\lim_{x\to a}f(x) = L$ iff, both $\lim_{x\to a^+} f(x) =L = \lim_{x\to a^-} f(x)$.

**Def:** Let $f: D\subseteq \Bbb R\to\Bbb R^n$, and $a \in D$, $f$ is said to be continuous on $a$ iff $(a_k) \subseteq D$ and $a_k \to a$, then $f(a_k) \to f(a)$.

********Th:******** Let $f, g:D\subseteq\Bbb R\to\Bbb R^n$, and $a$ be a cluster point of $D$ where $\lim_{x \to a}f(x) = L$ and ${\lim_{x\to a} g(x) = M}$:

- $\lim_{x\to a} (f+g)(x) = L+M$
- $\lim_{x\to a}(f\cdot g)(x) = L \cdot M$
- Let $c \in \Bbb R$, then $\lim_{x\to a} (cf)(x) = cL$
- Let $\phi:D\subseteq \Bbb R \to \Bbb R$, $\lim_{x\to a} \phi(x) = k$ then $\lim_{x\to a }(\phi f)(x) = k L$

******Def:****** Let $f: D\subseteq \Bbb R\to\Bbb R^n$, and $a \in D$, $f$ is continuous on $a$ iff for every $1 \le i \le n$, each coordinate function $f_i$ is continuous on $a$.

********Cor:******** Let $f: D\subseteq \Bbb R\to\Bbb R^n$, and $a\in D$, then $f$ is continuous at $a$ iff:

$$ \forall\varepsilon >0\exists>0\forall x\in D[|x-a|<\delta \implies \|f(x) - f(a)\| < \varepsilon] $$

********Cor:******** Let Let $f: D\subseteq \Bbb R\to\Bbb R^n$, and $a\in D$, then $f$ is continuous at $a$ iff ${\lim_{x\to a} f(x) = f(a)}$.

********Def:******** Let $f: D\subseteq \Bbb R\to\Bbb R^n$ is said to be continuous on $D$ if it is continuous at every $a \in D$.

**Cor:** Let $f, g: D\subseteq \Bbb R\to\Bbb R^n$ and $\phi:D\subseteq \Bbb R\to\Bbb R$ be continuous on $a\in D$. Then, $\phi f$, $f+g, f\cdot g$ are also continuous at $a \in D$.

********Def:******** Let $f: D\subseteq \Bbb R\to\Bbb R^n$, and $a\in D$, $f$ has a **removable discontinuity** if $f$ is discontinuous at $a$, but $\lim_{x\to a} f(x)=q \in \Bbb R^n$. This means $f$ can be modified to be continuous at $a$ by changing its value.