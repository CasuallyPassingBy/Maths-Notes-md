---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Jordan Measure]], [[Riemann Integral in Rn]], [[Sets of Measure Zero in Rn]]

**Def:** Let $f:A\subseteq\Bbb R^n \to \Bbb R$ be bounded over $A$. We define $f_A: \Bbb R^n\to \Bbb R$ as
$$ f_A(x) =\begin{dcases} f(x) & x\in A \\ 0 & x\not \in A \end{dcases} $$

We say that $f$ is integrable over $A$ if the function $f_A$ is integrable over a rectangle $R$ that contains $A$. In this case the integral of $f$ over $A$ is given by:
$$ \int_A f = \int_R f_A $$

Similarly, we prove that no matter the rectangle $R$ that contains $A$, we will obtain the same quantity ensuring the integral of $f$ over $A$ is well-defined.

**Def:** A subset $D\subseteq \Bbb R^n$ will be called a *domain of integration* if $D$ is bounded and has $\partial D$ has $n$-dimensional measure zero. 

**************Lemma:************** Let $f:A\subseteq \Bbb R^n\to \Bbb R$ be bounded over $A$ and $R$ a rectangle such that $A \subseteq R$. Then $D(f_A, R) \subseteq \text{Fr}(A) \cup D(f, A)$.

**Prop:** If $D \subseteq \Bbb R^n$ is a domain of integration, then every bounded continuous function on $D$ is integrable over $D$.

**Cor:** If $D\subseteq \Bbb R^n$ is a compact domain of integration then every continuous function on $D$ is integrable over $D$. 

**Th:** Let $f:A\subseteq \Bbb R^n\to \Bbb R$ be bounded over $A$, a Jordan-measurable set. If the set of discontinuities of $f$ over $A$, $D(f, A)$, is Jordan-measurable. Then $J(D(f, A))=0$, then $f$ is integrable over $A$.

**************Cor:************** Let $f:A\subseteq \Bbb R^n\to \Bbb R$ be bounded over $A$, a Jordan-measurable set. If $f$ is continuous over $A$, then $f$ is integrable over $A$.

- Algebraic Properties of the Integral over Jordan-measurable sets
    **Th:*** Let $f, g :A\subseteq \Bbb R^n\to \Bbb R$, then
    - $f+g$ is integrable over $A$ and $$ \int_A f+g = \int_A f+\int_A g $$
    - If $c \in \Bbb R$, then $cf$ is integrable over $A$ and $$ \int_A f = c\int_A f $$
    - $f^2$ is integrable over $A$
    - $fg$ is integrable over $A$
    - $|f|$ is integrable over $A$ and$$ \left|\int_A f\right|\le \int_A |f| $$
    - $f \ge 0$ then$$ \int_A f \ge 0 $$
    - $f\ge g$ then $$ \int_A f \ge \int_A g $$
    - the functions $\max\{f,g\}$ and $\min\{f,g\}$ are integrable over $A$

**Mean Value Theorem for Integrals:** Let $f,g:A\subseteq\Bbb R^n\to \Bbb R$ such that $f$ is continuous over $A$ and $g$ is integrable over $A$, with $A$ being a connected set. Then
- $\int_A f = f(x_0) \cdot J(A)$ for some $x_0 \in A$
- if $g\ge 0$ then $\int_A fg = f(x_0) \int_A g$ for some $x_0 \in A$

********Th:******** If $f:A\cup B \subseteq\Bbb R^n\to \Bbb R$ be integrable over $A$ and $B$, then $f$ is integrable over $A\cup B$ and $A\cap B$, furthermore
$$ \int_{A\cup B} f = \int_A f+ \int_B f-\int_{A\cap B}f $$

**Def:** Let $S\subseteq \Bbb R^k$ be any subset, and for each integer $n \ge 1$ suppose that $f_i: S \to \Bbb R^m$ is a function on $S$. 
- The sequence $\{f_n\}$ is said to *converge pointwise* to $f:S \to\Bbb R ^m$ if for every $a\in S$ and each $\varepsilon>0$, there exists an integer $N$ such that $n\ge  N$ implies $|f_n(a) - f(a)| < \varepsilon$.
- The sequence is said to *converge uniformly* to $f$ if $N$ can be chosen independently of the point $a$: For each $\varepsilon>0$, there exists $N$  such that $n \ge N$ implies $|f_n(a) - f(a) |<\varepsilon$ for every $a\in S$. 
- The sequence is *uniformly Cauchy* if for any For each $\varepsilon>0$, there exists $N$  such that $n , m\ge N$ implies $|f_n(a) - f_m(a)|< \varepsilon$ for all $a\in S$.

**Properties of Convergence:** Let $S\subseteq \Bbb R^k$ and suppose $f_n: S\to \Bbb R^m$ is continuous for each $n \ge 1$. 
1. If $f_n \to f$ uniformly, then $f$ is continuous.
2. If the sequence $\{f_n\}$ is uniformly Cauchy, then it converges uniformly to a continuous function.
3. If $f_n \to f$ uniformly and $S$ is a compact domain of integration, then $$\lim_{n \to \infty}\int_S f_n = \int_S f.$$
4. If $S$ is open, each $f_n$ is of class $\cal C^2$, $f_n \to f$ pointwise and $\{\partial f_n/\partial x^i\}$ converges uniformly on $S$ as $n \to\infty$, then $\partial f/\partial x^i$ exists on $S$ and $$\frac{\partial f}{\partial x^i} = \lim_{n \to\infty} \frac{\partial f_n}{\partial x^i}$$
We know that $1.$ and $4.$ are just [[Uniform Convergence In Metric Spaces#^09cab8|corollaries]] from metric spaces. Additionally, we know again from [[Complete Function Spaces#^3614fa|analysis]] that $2.$ is true. Lastly, we know that $3.$ is true because the proof is really similar to the [[Interchange of Limits#Integrable Limit Theorem|1 dimensional case]]. 