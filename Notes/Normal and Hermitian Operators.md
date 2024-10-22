---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Adjoint Operators and Matrices]]
### Normal Operators

**Def:** Let $V$ be an inner product space, and let ${T \in \mathcal L(V)}$. We say that $T$ is _********normal********_ if

$$ TT^* = T^* T $$

Similarly, $A \in \mathcal M_n(\mathbb F)$, $A$ is **normal** if

$$ A^* A= A A^* $$

********Th:******** Let $V$ be an inner product space, and let $T \in \mathcal L(V)$ be normal. Then the following are equivalent:
- $\|Tv\| = \|T^*v\|$ for all $v \in V$
- $T -\lambda I$ is normal for every $\lambda \in \mathbb F$
- If $v$ is an eigenvector of $T$ corresponding to eigenvalue $\lambda$, then $v$ is also an eigenvector of $T^*$ corresponding to $\overline \lambda$. That is, if $Tv = \lambda v$, then ${T^* v =\overline \lambda v}$.
- If $\lambda_1$ and $\lambda_2$ are distinct eigenvalues of $T$ with corresponding eigenvectors $v_1$ and $v_2$, then $v_1$ and $v_2$ are orthogonal.

********Th:******** Let $V$ be a finite dimensional complex inner product space and $T \in \mathcal L(V)$. $T$ is normal iff there exists an orthonormal basis for $V$ consisting of eigenvectors of $T$.

### Hermitian Operators

**Def:** Let $V$ be an inner product space and $T \in\mathcal L(V)$. We say that $T$ is **Hermitian or self-adjoint** if $T = T^*$. A matrix $A \in \mathcal M_n(\mathbb C)$ is **Hermitian** or **self-adjoint** if $A =A^*$.

**Th:** Let $V$ be an inner product space, and $T \in \mathcal L(V)$ is self-adjoint then every eigenvalue of $T$ is real.

********Th:******** Suppose $V$ is a complex inner product space and $T \in \mathcal L(V)$. Then $T$ is Hermitian iff, for every $v \in V$

$$ \langle Tv, v\rangle \in \Bbb R $$

Suppose $T$ is a self-adjoint operator on $V$ such that for all $v \in V$

$$ \langle Tv, v\rangle =0 $$

Then $T=0$.

********Th:******** Suppose $T \in \mathcal L(V)$ is self-adjoint and $b,c \in\Bbb R$ such that ${b^2 < 4c}$. Then

$$ T^2 +bT +cI $$

is invertible.

********Th:******** Suppose $V \ne \{0\}$, but finite dimensional, and $T \in \mathcal L(V)$ is a self-adjoint operator. Then $T$ has an eigenvalue.

********Th:******** Suppose $T \in \mathcal L(V)$ is a self-adjoint and $U$ is a subspace of $V$ that is $T$ invariant. Then:

- $U^\bot$ is $T$ invariant
- $T|_U \in \mathcal L(U)$ is self-adjoint
- $T|_{U^\bot} \in \mathcal L(U^\bot)$ is self-adjoint

********Th:******** Let $V$ a finite dimensional real inner product space . Then the characteristic polynomial of $T$, $\chi_T$, splits.

********Th:******** Let $V$ a finite dimensional real inner product space, and $T \in \mathcal L(V)$. Then $T$ is self-adjoint iff there exists an orthonormal basis $\beta$ for $V$ consisting of eigenvectors of $T$.