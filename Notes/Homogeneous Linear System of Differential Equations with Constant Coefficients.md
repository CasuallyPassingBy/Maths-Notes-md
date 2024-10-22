---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[Linear System of Ordinary Differential Equations]], [[Jordan Normal Form#Matrix Exponential|Matrix Exponential]], [[Complexification of Real Vector spaces]], [[Matrix Representation of Complex Numbers]]

We will concentrate most of our attention on system of homogeneous linear equations with constant coefficients, that is, the system of the form $$x' = Ax$$
where $A$ is a constant $n\times n$ matrix.

The equilibrium solutions are found by solving $Ax = 0$. We usually assume that $\det A \ne0$, so $x = 0$ is the only equilibrium solution. An important question is weather other solutions approach this equilibrium solution or depart from it as $t$ increases. Basically, is $x  = 0$ asymptotically stable or unstable? Or are there more possibilities?

For $n = 2$ is particularly important and leads to visualisation in the $x_1x_2$-plane, called the *phase plane*. By evaluating $Ax$ at a large number of points and plotting the resulting vectors we obtain a direction field of tangent vectors to solution of the system of differential equations. A qualitative understanding of the behaviour of solutions can be usually gained from a direction field. 

A plot that shows a representative sample of trajectories for a given system is called a *phase portrait*. 

Just as we did for the simpler case we will just assume that the solution involves an exponential, and we will multiply with a constant vector $x_0$. Then we propose $$x =x_0 e^{\lambda t}$$where $x_0$ and $\lambda$ are to be determined. If we substitute into the differential equation, and simplify we get that $$Ax_0 = \lambda x_0$$
Meaning that we have to find the eigenvalues and corresponding eigenvectors. 

If we assume that $A$ is a real-valued matrix, there are three possibilities for the eigenvalues of $A$:
- All eigenvalues are real and different from each other
- Some eigenvalues occur in complex conjugate pairs
- Some eigenvalues are repeated

### All Eigenvalues are real and different

Then associated with each eigenvalue $\lambda_i$ is a real eigenvector $v^{(i)}$, and the $n$ eigenvectors are clearly linearly independent. The corresponding solutions of the differential equation are $$x^{(k)} = v^{(k)} e^{\lambda_k t}\quad\qquad k \in \{1, \dots, n\} $$
We see that $W[x^{(1)}, \dots, x^{(n)}](t) = \exp((\lambda_1 + \dots + \lambda_n)t)W[x^{(1)}, \dots, x^{(n)}](0)$. Since they are linearly independent, then $W[x^{(1)}, \dots, x^{(n)}](0)\ne 0$. Then $x^{(1)}, \dots, x^{(n)}$ form a fundamental set of solutions and $$x = \sum_{k = 1}^n c_k v^{(k)}e^{\lambda_k t} $$
### Complex Eigenvalues

We know that if $A$ is real matrix, and has one complex eigenvalue then there's at least its conjugate pair. We know by the [[Complexification of Real Vector spaces]].

Suppose that there is a pair of complex conjugate eigenvalues $\lambda = a+ib$ and $\overline \lambda$. Then there exists their corresponding eigenvector $v$ and $\overline v$  

then we have the solutions $$x^{(1)} = v e^{\lambda t} \qquad x^{(2)} = \overline v e^{\overline \lambda t}$$
We can consider, more practical vectors mainly $\Re(x^{(1)})$ and $\Im(x^{(1)})$. These are linear combinations of $x^{(1)}$ and $x^{(2)}$, and are linearly independent. We can see that the imaginary portion of the eigenvalue actually makes the solution rotate around the origin, while the real part makes it get closer or get farther away from the origin. 

A more general way to solve the systems is in [[Fundamental Matrices for Linear System of Differential Equations]]
