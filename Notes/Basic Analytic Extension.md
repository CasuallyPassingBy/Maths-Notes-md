---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Analytic Functions]], [[2D Harmonic Functions]]
## Reflection along Lines

Let $U\subseteq \Bbb C$ be a region, and we define $U^*$ as
$$
U^*:= \{z \in \Bbb C \mid \overline z \in U\}
$$
If $U = U^*$ we say that $U$ is symmetrical with respect to the real line.

We are going to use a special  for this part
- $U^+:= \{z \in U \mid \Im z > 0\}$
- $U^0:= \{z \in U \mid \Im z = 0\}$
- $U^-:= \{z \in U \mid \Im z < 0\}$

Let $U = U^*$ be a region, and $v = : U^+\cup U^0 \subseteq \Bbb C\to \Bbb R$ continuous and $v \in a(U^+)$. If $v|_{U^0} \equiv 0$ then, there's a function $\tilde v: U \subseteq \Bbb C\to \Bbb R$ harmonic, and $\tilde v|_{U^+\cup U^0} = v$ with for all $z \in U$ we have that $\tilde v (z) = -\tilde v(\overline z)$. Meaning that the extension of $v$ is given by the formula:
$$
\tilde v(z) )=
\begin{cases}
v(z) & z \in U^+\cup U^0 \\ \\
-v(\overline z) & z \in U^-
\end{cases}
$$
### Schwarz Reflection Principle
Let $U = U^*$. If $f:U^+\cup U^0\subseteq \Bbb C \to \Bbb C$ continuous and analytic on $U^+$ with $f[U^0] \subseteq \Bbb R$, then there's a function $g: U \subseteq \Bbb C \to \Bbb C$ analytic on $U$ such that $g|_{U^+\cup U^0} =f$, meaning $g$ is an analytic extension of $f$ onto $U$, and $g$ is given by the relation
$$
g(z) = 
\begin{cases}
f(z) & z \in U^+\cup U^0 \\ \\
\overline{f(\overline z)} & z \in U^-
\end{cases}
$$
This can generalised to more circles
## Circle Inversion

We say $U\subseteq \Bbb C$ be a region, we define 
$$
\tilde U :=\left\{z \in \Bbb C \;\left|\;\frac{1}{\overline z} \in U\right.\right\}
$$
is the image of the inversion along the unit circle. If $U =\tilde U$ , we say that $U$ is symmetric with respect to $\partial D$, where $D = B_1(0)$. 

### Principle of Circle Inversion

Let $D = B_1(0)$, and $U \subseteq \Bbb C$, such that $U = \tilde U$, $0\not\in U$. If $f:U \cap \overline D\to C$ continuous and analytic on $U\cap D$, with $f:[U \cap \partial D]\subseteq \Bbb R$, then there's a function $g:U \to \Bbb C$ analytic such that $g|_{U \cap D} = f$, given by the formula
$$
g(z) =
\begin{dcases}
f(z) & z \in U \cap D\\
\\
\overline{f\left(\frac{1}{\overline z}\right)} &z \in U \setminus D
\end{dcases}
$$
This can generalised to more circles