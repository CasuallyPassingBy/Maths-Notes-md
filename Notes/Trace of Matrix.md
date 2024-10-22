---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Determinants]], [[Eigenvalues]], [[Jordan Normal Form]], [[Gauss's Theorem and Divergence in R3]], [[Divergence Theorem in R2]]

The *trace* of an $n\times n$ square matrix $A$ is defined as $$\text{tr}(A) = \sum_{i = 1}^n a_{ii}$$
We have that is has a couple of easy properties:
- $\text{tr}(A+B) = \text{tr}(A) + \text{tr}(B)$
- $\text{tr}(cA) = c\text{tr}(A)$ 
Where $A$ and $B$ are square matrices and $c$ a scalar.

Similarly, we have that $$\text{tr}(A) = \text{tr}\left(A^\top\right)$$
An important property, let $A$ and $B$ be square matrices, then $$\text{tr}(AB) = \text{tr}(BA)$$
**Cor:** There do not exist operators $S, T \in \mathcal L(V)$ such that $ST-TS = I$, or $[S, T] = I$ using the commutator notation. 

Let $P$ be a change of basis matrix then with $A= PBP^{-1}$, then $$\text{tr}(A) = \text{tr}(PBP^{-1}) = \text{tr}(BP^{-1}P) = \text{tr}(B)$$
With this we can define the trace of an operator, let $T\in \mathcal L(V)$ and $\beta$ a basis of $V$, then $$\text{tr}(T) := \text{tr}([T]_\beta) $$
with this if we are over an algebraicly closed field we get that, if $T$ is a linear operator with $\lambda_1, \dots, \lambda_n$ are the eigenvalues of $T$, then $$\text{tr}(T) = \sum_{i = 1}^n\lambda_i$$
We get a nice connection between the determinan, using [[Jordan Normal Form#Matrix Exponential|the matrix exponential function]], getting that $$\det(\exp(A)) = \exp(\text{tr}(A))$$
A related characterisation of the trace applies to linear vector fields. Given a matrix $A$, define the vector field $F: \Bbb R^n \to \Bbb R^n$ by $F(x) = Ax$. The components of this vector field are linear functions (given by the rows of $A$). Its divergence $\text{div} F$ 
is a constant function, whose value is $\text{tr}(A)$. 

