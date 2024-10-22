---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Eigenvalues]], [[Eigenspaces and Diagonal Matrices]], [[Nilpotent Linear Operators]], [[Characteristic and Minimal Polynomial of a Linear Transformation]]

********Def:******** Let $T \in \mathcal L(V)$ and $\lambda$ is an eigenvalue of $T$. A vector $v \in V$ is called a *generalised eigenvector* of $T$ corresponding to $\lambda$ if $v \ne 0$ and

$$ (T-\lambda I)^k v =0 $$

for some $k \in \Bbb N^+$

**Def:** Suppose $T \in \mathcal L(V)$ and $\lambda \in \Bbb F$. The *generalised eigenspace* of $T$ corresponding to $\lambda$, denoted $G(\lambda, T)$ is defined to be the set of all generalised eigenvectors of $T$ corresponding to $\lambda$, along with the $0$ vector. From this definition, it is easy to see that $E(\lambda, T) \subseteq G(\lambda, T)$

**Th:** Suppose $T \in \mathcal L(V)$ and $\lambda \in \Bbb F$, and $V$ is a finite dimensional vectors space. Then

$$ G(\lambda, T) = N((T-\lambda I)^{\dim V}) $$

**Th:** Let $T \in \mathcal L(V)$, and let $\lambda$ be an eigenvalue of $T$. Then
- $G(\lambda, T)$ is a $T$-invariant subspace of $V$ containing $E(\lambda, T)$
- For any eigenvalue of $T$ such that $\mu \ne \lambda$    $$ G(\mu, T) \cap G(\lambda, T) = \{ 0\} $$
- For any scalar $\mu \ne \lambda$ , the restriction $T - \mu I$ to $G(\mu, T)$ is a bijection

There are two kinds of multiplicities,

- Algebraic multiplicity of $\lambda = \dim G(\lambda, T)$
- Geometric multiplicity of $\lambda = \dim E(\lambda, T)$

********Th:******** Let $T$ be linear operator on a finite-dimensional vector space $V$ such that $\chi_T$ splits. Suppose that $\lambda$ is an eigenvalue of $T$ with multiplicity $m$. Then
- $\dim G(\lambda, T) \le m$
- $G(\lambda, T) = N((T-\lambda I)^{m})$

********Th:******** Suppose $T \in \mathcal L(V)$, with $V$ being a finite dimensional vector space such that $\chi_T$ splits. Let $\lambda_1, \dots, \lambda_k$ be distinct eigenvalues of $T$. Then
- each $(T- \lambda_i I)|_{G(\lambda_i, T)}$ is nilpotent
    
- there exists unique vectors $v_i \in G(\lambda_i , T)$ for all $i$ such that for all $x \in V$
    $$ x = v_1+v_2 \dots +v_k $$
    

********Th:******** Let $T$ be a linear operator on a finite-dimensional vector space $V$ whose characteristic polynomial $(t -\lambda_1)^{m_1} (t -\lambda_2)^{m_2}\cdots (t -\lambda_k)^{m_k}$ splits. For $i = 1, 2, ... , k$ , let $\beta_i$ be an ordered basis for $G(\lambda_i, T)$. Then

- $\beta_i \cap \beta_j = \varnothing$ for $i \ne j$
- $\beta = \beta_1 \cup \dots \cup \beta_k$ is an ordered basis of $V$
- $\dim G(\lambda_i, T) = m_i$ for all $i$

**Cor:** Suppose $T \in \mathcal L(V)$, with $V$ being a finite dimensional vector space such that $\chi_T$ splits. Then $T$ is diagonalizable iff $E(\lambda, T) = G(\lambda , T)$

********Th:******** Suppose $T \in \mathcal L(V)$, with $V$ being a finite dimensional vector space such that $\chi_T$ splits. Then there is a basis of $V$ consisting of generalised eigenvectors of $T$

**Def:** Let $T \in \mathcal L(V)$, and let $x$ be a generalised eigenvector of $T$ corresponding to the eigenvalue $\lambda$. Suppose that $p$ is the smallest positive integer for which $(T-\lambda I)^p (x) =0$. Then the ordered set

$$ \{(T-\lambda I)^{p-1} (x), \dots, (T-\lambda I) (x), x\} $$

is called **cycle of generalised eigenvectors** of $T$ corresponding to $\lambda$. The vectors ${(T-\lambda I)^{p-1}(x)}$ and $x$ are called the _initial vector_ and the _end vector_ of the cycle, respectively. We say the _length_ of the cycle is $p$

********Th:******** Let $T$ be a linear operator on a finite-dimensional vector space $V$ whose characteristic polynomial splits, and suppose that $\beta$ is a basis for $V$ such that $\beta$ is a disjoint union of cycles of generalised eigenvectors of T. Then the following statements are true.

- For each cycle $\gamma$ of generalised eigenvectors contained in $\beta$, $W=\operatorname{span} \gamma$ is $T$-invariant, and $[T|_W]_\gamma$ is a Jordan block
- $\beta$ is a Jordan canonical basis for $V$

********Th:******** Let $T\in \mathcal L(V)$, and let $\lambda$ be an eigenvalue of $T$. Suppose $\gamma_1, \gamma_2, \dots, \gamma_q$ are cycles of generalized eigenvectors of $T$ corresponding to $\lambda$ such that the initial’s vector of the $\gamma_i$’s are distinct and form a linearly independent set. Then the $\gamma_i$’s are disjoint, and

$$ \gamma = \bigcup_{i = 1}^q \gamma_i $$

is their union

********Cor:******** Every cycle of generalized eigenvectors of a linear transformation is linearly indpendent

********Th:******** Let $T$ be a linear operator on a finite-dimensional vector space $V$, and let $\lambda$ be an eigenvalue of $T$. Then $G(\lambda, T)$ bas an ordered basis consisting of a union of disjoint cycles of generalized eigenvectors corresponding to $\lambda$

**Cor:** Let $T$ be a linear operator on a finite-dimensional vector space $V$ whose characteristic polynomial splits. Then T bas a Jordan canonical form.

**Def:** Let $A \in \cal M_n (\Bbb F)$ be such that the characteristic polynomial splits. Then the **Jordan canonical form** of $A$ is defined to be the Jordan canonical form of the linear operator $L_A$ on $\Bbb F^n$

**Cor:** Let $A \in \cal M_n (\Bbb F)$ be such that the characteristic polynomial splits. Then $A$ has a Jordan canonical form $J$, and $A$ is similar to $J$

********Th:******** Suppose $T \in \mathcal L(V)$, with $V$ being a finite dimensional vector space such that $\chi_T$ splits. Let $\lambda_1, \dots, \lambda_k$ be distinct eigenvalues of $T$. Then $V= \bigoplus_{i = 1}^k G(\lambda_i , T)$

**Cor:** Let $T$ be a linear operator on a finite-dimensional vector space $V$ such that the characteristic polynomial of $T$ splits, and let $\lambda_1, \dots, \lambda_m$ be the distinct eigenvalues of $T$. For each $i$, let $J_i$ be the Jordan canonical form of the restriction of $T$ to $G(\lambda_i, T)$ . Then

$$ J = J_1 \oplus J_2 \oplus \dots \oplus J_k $$

and $J$ is the canonical form

The most important thing is to find a Jordan canonical basis for $T$ of $G(\lambda_i, T)$, for all eigenvalues of $T$. Then we can get the basis for all the space by joining them together.

Let $T_i = T|_{G(\lambda_i, T)}$, for the sake of simplicity, and we will use a dot diagram (Ferrer’s diagram) of $T_i$. Suppose that $\beta_i$ is a disjoiint union of cycles generated by eigenvector $\gamma_1, \dots, \gamma_{n_i}$ with lengths $p_1 \ge p_2\ge \dots\ge p_{n_i}$. The dot diagram of $T_i$ contains one dot for each vector in $\beta_i$, and the dots are configured according to the following rules

- The array consists of $n_i$ columns (one for each cycle)
- Counting from left to right, the $j$th column consists of the $p_j$ dots that correspond to the vectors of $\gamma_j$ starting with the initial vector at the top and continuing down to the end vector

If we denoted $v_1, \dots, v_{n_i}$ end vectors of the cycles. The following dot diagram of $T_i$, each dot is labelled with the name of the vector in $\beta_i$ to which corresponds

$$ \begin{array}{cccc} \bullet (T-\lambda_i I)^{p_1-1}(v_1)& \bullet (T-\lambda_i I)^{p_2-1}(v_2)& \cdots & \bullet (T-\lambda_i I)^{p_{n_i}-1}(v_{n_i})\\

\bullet (T-\lambda_i I)^{p_1-2}(v_1)& \bullet (T-\lambda_i I)^{p_2-2}(v_2)& \cdots & \bullet (T-\lambda_i I)^{p_{n_i}-2}(v_{n_i})\\ &&& \vdots \\ &\vdots&& \bullet (T- \lambda_iI)(v_{n_i}) \\

\vdots&&& \bullet v_{n_i} \\ & \bullet (T-\lambda_i I) (v_2) \\ & \bullet v_2 & \\ \bullet(T-\lambda_i I) (v_1) \\ \bullet v_1\\ \end{array} $$

The dot diagram of $T_i$ has $n_i$ columns, and $p_1$ rows. Now let $r_j$ denote the number of dots in the $j$th row of thw dot diagram. We get that ${r_1 \ge r_2 \ge \dots \ge r_{p_1}}$. Furthermore, the diagram can be reconstructed from $r_j$ ’s. Since it can be considered the transpose of the Ferrers’s diagram.

**Th:** For any positive integer $r$, the vectors in $\beta_i$, that are associated with dots in the $r$ rows of the dot diagram of $T_i$ constitute a basis for ${N((T-\lambda_i I)^r)}$. Hence the number of dots in the first $r$ of the dot diagram equals $\dim {N((T-\lambda_i I)^r)}$.

**Cor:** The dimension of $E(\lambda_i, T)$ is $n_i$. Hence in a Jordan canonical form of $T$, the number of Jordan blocks corresponding to $\lambda_i$ equals the dimension of $E(\lambda_i, T)$

********Th:******** Let $r_j$ denote the number of dots in the $j$th row of the dot diagram of $T_i$, the restriction of $T$ to $G(\lambda_i, T)$. Then the following statements are true

- $r_1 = \dim V -\dim R( T- \lambda_i I)$
- $r_j = \dim R(T-\lambda_i I) ^{j-1}-\dim R(T-\lambda_i I) ^{j}$

********Cor:******** For any eigenvalue $\lambda_i$ of $T$, the dot diagram of $T_i$, is unique. Thus, subject to the convention that the cylces of generalized eigenvectors for the bases of each of each generalized eigenspace are listed in order of decreasing length, the Jordan canonical form of a linear operator or a matrix is unique up to reordering of the eigenvalues

### How to get the Jordan normal basis
The way to actually calculate the Jordan normal basis, is first calculating the basis for $E(\lambda, T)$ for any eigenvalue $\lambda$ of $T$. Then if $v_1$ is a member of the basis, then the way is to solve the linear equation

$$ (T-\lambda I) v_2 = v_1 $$

if it has no solution, then you know that $v_1$, is the only member in the cycle. If it has a solution, then we solve inductively

$$ (T-\lambda I) v_{i+1}= v_i $$

till we can’t solve any more or we know we have enough generalized eigenvectors. In general when we look at

$$ (T-\lambda I)^{-1}[\{v_i\}] = v_{i+1} +E(\lambda, T) $$

and we can ignore any vector the term of $E(\lambda, T)$.
## Jordan Block Powers and Limits
If we look at a jordan block it will be of the following form for an eigenvalue $\lambda$

$$ \begin{pmatrix} \lambda &1 & 0&\cdots & 0 \\ 0 & \lambda & 1 &\cdots & 0\\ 0 & 0 &\lambda &\cdots & 0 \\ \vdots & \vdots &\vdots & &\vdots \\ 0 & 0 &0 &\cdots &1 \\ 0 & 0 &0 &\cdots &\lambda

\end{pmatrix} $$

Then we can see that we can write $A$, as a sum of a diagonal matrix $D$ and a nillpotent one $M$. In general, if $J =[T]_\beta$, with $\beta$ being the Jordan canonical basis, then $J = D+M$, with $D$ being a diagonal matrix, and $M$ being a nilpotent one, such that $DM =MD$. If $p$ is the smallest integer such that $M^p =O$, then for any $r$ positive integer
$$ J^r = \sum_{k = 0}^{\min\{r, p-1\}} {r\choose k} D^{r-k} M^k $$

We can see that $\lim_{n \to \infty } J^n$ exists if for all Jordan blocks $A$, $\lim_{n \to \infty} A^n$ exists. Then, if ${A = \lambda I +N}$ is an $m \times m$ Jordan block, $\lim_{n \to \infty} A^n$ exists iff
- $|\lambda| < 1$
- $\lambda =1$ and $m =1$

### Matrix Functions
Let $A \in \cal M_n (\Bbb C)$ be a transition matrix. Since $\Bbb C$ is an algebraically closed field, $A$ has a Jordan canonical form $J$ to which $A$ is similar. Let $P$ be an invertible matrix such that $P ^{-1} AP = J$.
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
## [[Markov Chains with Matrices]]

**Def:** Let $A \in \cal M_n (\Bbb C)$, we define the norm of $A$ by

$$ \|A\|_m = \max_{1 \le i,j \le n} |A_{ij}| $$

**Prop:** Let $A, B \in \cal M_n (\Bbb C)$
- $\|A\|_m \ge0$
- $\| A\|_m = 0$ iff $A = O$
- $\| cA\|_m = |c| \cdot \|A\|_m$
- $\|A+B\|_m \le \|A\|_m+\|B\|_m$
- $\|AB\|_m \le n \|A\|_m\|B\|_m$

Let $A \in \cal M_n (\Bbb C)$ be a transition matrix. Since $\Bbb C$ is an algebraically closed field, $A$ has a Jordan canonical form $J$ to which $A$ is similar. Let $P$ be an invertible matrix such that $P ^{-1} AP = J$.

- $\| A^k \| \le 1$ for any positive integer $k$
- There exists a positive number $c$ such that $\| J^k \| \le c$ for every positive integer $k$
- Each Jordan block of $J$ corresponding to the eigenvalue $\lambda = 1$ is a $1 \times 1$ matrix
- $\lim_{k \to \infty} A^k$ exists if and only if $1$ is the only eigenvalue of $A$ with absolute value $1$