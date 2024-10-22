---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Vector Spaces]], [[Eigenspaces and Diagonal Matrices]], [[Characteristic and Minimal Polynomial of a Linear Transformation]], [[Eigenvalues]], [[Jordan Normal Form]]

**Def**: Suppose $V$ a real vector space:
- The *complexification* of $V$, denoted as $V_\Bbb C$ equals $V \times V$. An element of $V_\Bbb C$ is an ordered pair $(u, v)$ where $u, v \in V$, but we will write this as $u +iv$
- Addition on $V_\Bbb C$ is defined by $$(u_1+iv_1) + (u_2+iv_2) = (u_1+u_2)+i(v_1+v_2)$$for $u_1, u_2, v_1, v_2 \in \Bbb C$
- Complex scalar multiplication on $V_\Bbb C$ is defined by$$(a+ib)(u+iv) = (au-bv)+i(av+bu)$$
**Prop:** Suppose $V$ a real vector space. Then with the definitions of addition and scalar multiplication as above, $V_\Bbb C$ is a complex vector space

**Prop:** Suppose $V$ a real vector space. 
- if $v_1, \dots, v_n$ is a basis of $V$ (as a real vector space), then $v_1, \dots, v_n$ is a basis of $V_\Bbb C$ (as a complex vector space)
- The dimension of $V_\Bbb C$ (as a complex vector space) equals the dimension of $V$ (as a real vector space)


**Def:** Suppose $V$ a real vector space and $T \in \mathcal L(V)$. The *complexification* of $T$, denoted as $T_\Bbb C$, is the operator $T_\Bbb C \in \mathcal L(V_\Bbb C)$ defined by $$T_\Bbb c(u+iv) = Tu+iTv$$for $u, v \in V$.

**Prop:** Suppose $V$ a real vector space with a basis $\beta$ and $T\in \mathcal L(V)$. Then $[T]_\beta = [T_\Bbb C]_\beta$

**Prop:** Every operator on a nonzero finite-dimensional vector space has invariant subspace of dimension $1$ or $2$.

### Minimal Polynomial

Suppose $V$ a real vector space and $T\in \mathcal L(V)$. Repeated application of $T_\Bbb C$ shows that $$(T_\Bbb C) (u+iv) = T^n u +i T^n v$$
for every positive integer $n$ and all $u, v \in V$. 

**Prop:** Suppose $V$ a real vector space and $T\in \mathcal L(V)$. Then the minimal polynomial of $T_\Bbb C$ equals the minimal polynomial of $T$. $\mu_{T_\Bbb C} = \mu_T$

Then we get that the minimal polynomial of $T_\Bbb C$ has real coefficients. 

### Eigenvalues and Generalised Eigenvalues

**Prop:** Suppose $V$ a real vector space, $T\in \mathcal L(V)$ and $\lambda \in \Bbb R$. Then $\lambda$ is an eigenvalue of $T_\Bbb C$ iff $\lambda$ is an eigenvalue of $T$

**Th:** Suppose $V$ a real vector space, $T\in \mathcal L(V)$, $\lambda \in \Bbb C$, $j \in \Bbb N$ and $u, v \in V$. Then $$(T_\Bbb C-\lambda I)^j(u+iv)  = 0 \iff (T_\Bbb C-\overline \lambda I)^j(u-iv)  = 0$$
**Cor:** Suppose $V$ a real vector space, $T\in \mathcal L(V)$, and $\lambda \in \Bbb C$. Then $\lambda$ is an eigenvalue of $T_\Bbb C$ iff $\overline \lambda$ is an eigenvalue of $T_\Bbb C$. Meaning that non-real eigenvalues of $T_\Bbb C$ come in pairs.

**Th:** Suppose $V$ a real vector space, $T\in \mathcal L(V)$, and $\lambda \in \Bbb C$ is an eigenvalue of $T_\Bbb C$. Then the multiplicity of $\lambda$ as an eigenvalue of $T_\Bbb C$ equals the multiplicity of $\overline \lambda$ as an eigenvalue of $T_\Bbb C$. 

**Cor:** Every operator on an odd-dimensional real vector space has an eigenvalue

### Characteristic Polynomial

**Prop:** Suppose $V$ a real vector space and $T\in \mathcal L(V)$. Then the coefficients of the characteristic polynomial of $T_\Bbb C$ are all real. 

**Def:** Suppose $V$ a real vector space and $T \in \mathcal L(V)$. The the *characteristic polynomial* of $T$ is defined to be the characteristic polynomial of $T_\Bbb C$. 

**Th:** Suppose $V$ a real vector space and $T\in \mathcal L(V)$
- the coefficients of the characteristic polynomial of $T$ are all real; $\chi_T \in \Bbb R[x]$
- the characteristic polynomial of $T$ has degree $\dim V$ 
- the eigenvalues of $T$ are precisely the real zeros of the characteristic polynomial