---
tags:
  - LinearAlgebra
  - StochasticProcesses
---
Subjects: [[Linear Algebra]], [[Stochastic Processes]]
Links: [[Matrix Limits]], [[Eigenspaces and Diagonal Matrices]]
**********Def:********** A vector in $\Bbb R^n$ with all nonnegative entries that sum up to $1$ is called a ******************probability vector.******************

**********Def:********** Let $M \in \cal M_n(\Bbb R)$ such that for all ${1\le i, j\le n}$, ${M_{ij}\ge 0}$ and for all ${1 \le j \le n}$, the column $M_{\cdot j}$ sums to $1$. Then $A$ is called a ******************transition matrix****************** or a _****************stochastic matrix****************_. For an arbitrary $n\times n$ transition matrix $M$, the rows and columns correspond to $n$ _******states******_, and the $M_{ij}$ represents the probability of moving from state $j$ to state $i$ in one _****stage****_.

********Th:******** Let $M \in \cal M_n(\Bbb R^\ge)$ and $v\in \Bbb R^n$ having nonnegative coordinates, and ${u \in \Bbb R^n}$ be the vector in which each coordinate equals $1$. Then

- $M$ is a transition matrix iff $u^\top M = u^\top$
- $v$ is a probability vector iff $u^\top v = 1$

********Cor:******** Transition matrices are closed under multiplication. In particular, closed under powers of a matrix. The product of a transition matrix and a probability vector is a probability vector.

**********Def:********** If the probability that an object in one states changes to a different state in a fixed interval of time depends only on time depends only on the two states, the stochastic process is called a _****Markov process****_. If in addition there’s only finitely many states is called a _**Markov chain.**_

************Def:************ A transition matrix is called ********regular******** if some power of the matrix contains only positive entries.

**********Th:********** Every transition matrix has $1$ as an eigenvalue, using [[Gershgorin’s Circle Theorem]]

********Th:******** Let $A \in \mathcal M_n(\mathbb C)$, be a matrix in which each entry is a positive real number, and $\lambda \in \mathbb C$ be an eigenvalue of $A$ such that ${|\lambda| = \rho(A)}$. Then ${\lambda = \rho(A)}$ and $\{u\}$ us a basis of $E(\lambda, A)$, where $u \in \mathbb C^n$ is the vector in which each coordinate equals $1$.

**********Cor:********** Let $A \in \mathcal M_n(\mathbb C)$, be a matrix in which each entry is a positive real number, and $\lambda \in \mathbb C$ be an eigenvalue of $A$ such that ${|\lambda| = \nu(A)}$. Then ${\lambda = \nu(A)}$ and ${\dim E(\lambda, A) =1}$

**********Cor:********** Let $A \in \mathcal M_n(\mathbb C)$ be a transition matrix in which each entry is positive and $\lambda$ be an eigenvalue other than $1$, then ${|\lambda| < 1}$. Moreover, then the eigenspace corresponding to the eigenvalue $1$ has dimension $1$.

********Th:******** Let $A$ be regular transition matrix, and $\lambda$ be an eigenvalue of $A$. Then

- $|\lambda| \le 1$
- If $|\lambda| = 1$, then $\lambda = 1$ and $\dim E(\lambda, A) = 1$

**********Cor:********** Let $A$ be a regular transition matrix that is diagonalizable. Then ${\lim_{n\to\infty}A^n }$ exists.

********Th:******** Let $A$ be a regular transition matrix. Then

- The multiplicity of $1$ as an eigenvalue of $A$ is $1$.
- $\lim_{n\to\infty} A^n$ exists
- $L = \lim_{n\to \infty} A^n$ is a transition matrix
- $AL =LA =L$
- The columns of $L$ are identical. In fact, each column of $L$ is equal to the unique probability vector $v$ that is also an eigenvector of $A$ corresponding to the eigenvalue $1$.
- For any probability vector $w$, $\lim_{n\to\infty }(A^n w) =v$

**********Def:********** The vector $v$ above is called the _**fixed probability vector**_ or _********stationary vector********_ of the regular transition matrix $A$.

**********Def:********** A transition matrix of the form

$$ \begin{pmatrix} I & B \\ O & C \end{pmatrix} $$

where $I$ is an identity matrix and $O$ is a zero matrix is another form of transition matrices. The states corresponding to the identity submatrix are called ****absorbing states****. A Markov chain is called an _****absorbing Markov chain****_ if it is possible to go from an arbitrary state unto an absorbing state in a finite number of stages.