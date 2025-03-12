---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Jordan Normal Form]], [[Normed Algebras]], [[Trace of Matrix]]

We have that $\mathcal M_n(\Bbb R)$ and $\mathcal M_n(\Bbb C)$ are normed algebras with the norm $$\|A \|= \sqrt{\sum_{i, j = 1}^n |a_{ij}|^2}$$and for matrices $A$ and $B$, we have that $\|AB\| \le \|A\| \|B\|$. 

Let $A \in \mathcal M_n (\Bbb C)$ be a transition matrix. Since $\Bbb C$ is an algebraically closed field, $A$ has a Jordan canonical form $J$ to which $A$ is similar. Let $P$ be an invertible matrix such that $P ^{-1} AP = J$.
If $f$ is an analytic function has [[Taylor Series in R|Taylor expansion]]

$$ f(x) = \sum_{k = 0}^\infty c_k x^k $$

then we can define a matrix function $A \mapsto f(A)$ can be defined by substitting $x$ by a square matrix: powers become matrix powers, addition be additions become matrix sums and multiplications by coefficients become scalar multiplications. If the series converges for $|x| <r$, then the corresponding matrix series converges for matrices such that $\|A \| <r$ for some matrix norm that satisfies $\|AB\| \le \|A \|\|B\|$

We can see that the function evaluated on a Jordan block we get that
$$ f \left( \begin{bmatrix}\lambda & 1       & 0      & \cdots & 0 \\0       & \lambda & 1      & \vdots & \vdots \\0       & 0       & \ddots & \ddots & \vdots \\\vdots  & \cdots  & \ddots & \lambda & 1 \\0       & \cdots  & \cdots & 0 & \lambda\end{bmatrix} \right) = \begin{bmatrix}\frac{f(\lambda)}{0!} & \frac{f'(\lambda)}{1!} & \frac{f''(\lambda)}{2!} & \cdots                & \frac{f^{(n)}(\lambda)}{n!} \\0                     & \frac{f(\lambda)}{0!}  & \frac{f'(\lambda)}{1!}  & \vdots                & \frac{f^{(n-1)}(\lambda)}{(n-1)!} \\0                     & 0                      & \ddots                  & \ddots                & \vdots \\\vdots                & \cdots                 & \ddots                  & \frac{f(\lambda)}{0!} & \frac{f'(\lambda)}{1!} \\0                     & \cdots                 & \cdots                  & 0                     & \frac{f(\lambda)}{0!}\end{bmatrix} $$
Where the derivative is with respect to $\lambda$, and if there were a multiple, like $t$ multiplying the block, then successive powers of $t$ would accompany it

# Matrix Exponential

**Def:** Let $A \in \mathcal M_n(\mathbb C)$, then we can define $e^A$ as follows:

$$ e^A:= \sum _{n= 0}^\infty \frac{1}{n!} A^n $$

If $A$ is diagonalizable, in particular $A = PDP^{-1}$, then we can calculate it as

$$ e^A = P e^DP^{-1} $$
Which can help to solve a [[Homogeneous Linear System of Differential Equations with Constant Coefficients]]. 

From these we can see that for any $A \in \cal M_n (\Bbb C)$, $\exp(A)$ exists, and we have the special property that $\det (\exp(A)) = \exp(\operatorname{tr}(A))$

We have that if $AB = BA$, then $\exp(A)\exp(B) = \exp(A+B)$.

**Prop:** For $X \in \mathcal M_n(\Bbb F)$ where $F = \Bbb R, \Bbb C$,  $$\frac{d}{dt} \exp(tX) = X\exp(tX) = \exp(tX)X$$
**Prop:** For $X \in \mathcal M_n(\Bbb F)$ where $F = \Bbb R, \Bbb C$, $\det (\exp(X)) = \exp(\text{tr}(X))$. 