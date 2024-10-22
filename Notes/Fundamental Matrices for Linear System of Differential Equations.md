---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[Linear System of Ordinary Differential Equations]], [[Jordan Normal Form#Matrix Exponential|Matrix Exponential]]

Let $x^{(1)}, \dots, x^{(n)}$ form a fundamental set of solutions for the equation $$x' = P(t)x$$
on some interval $(\alpha, \beta)$. Then the matrix $$X(t) = \Psi(t) = 
\begin{pmatrix}
x_1^{(1)}(t) &\cdots & x_1^{(n)}(t) \\
\vdots && \vdots \\
x_n^{(1)}(t) &\cdots & x_n^{(n)}(t) \\
\end{pmatrix}$$
whose columns are the vectors $x^{(1)}, \dots, x^{(n)}$ is said to be the *fundamental matrix* of the system. Note that the fundamental matrix is nonsingular since its columns are linearly independent vectors.

The solution of an initial value problem can be written very compactly in terms of the fundamental matrix. The general solution of $x' = P(t)x$ is $$x = \sum_{k = 1}^n c_k x^{(k)}$$or, in terms of $\Psi(t)$, $$x = \Psi(t) c$$where $c$ is a constant vector with arbitrary components $c_1, \dots, c_n$. For an initial value problem consisting of the differential equation $x' = P(t) x$ and the initial condition $$x(t_0) = x_0$$where $t_0 \in (\alpha, \beta)$ and $x_0$ is a given initial vector. We only need to choose an appropriate $c$ to satisfy the initial condition. Hence $$\Psi(t_0)  c = x_0$$Then $$c = (\Psi(t_0))^{-1}x_0$$and $$x = \Psi(t) (\Psi(t_0))^{-1} x_0$$
The each column of the matrix $\Psi$ is a solution to $x' = P(t) x$. it follows that $\Psi$ satisfies the matrix differential equation $$\Psi' = P(t) \Psi$$
If we consider the set of fundamental solutions such that $x^{(k)} = e_k$, where $e_1, \dots, e_n$ represents the canonical basis of $\Bbb R^n$. Then we have that $$\Phi(t_0 ) = I$$
For this note, I am going to reserve the symbol $\Phi$ to denote this fundamental matrix, and use $\Psi$ for an arbitrary fundamental matrix. Then we have that $(\Phi(t_0))^{-1} = I$, then it follows that $$x = \Phi(t) x_0$$
to calculate $\Phi$, we can just compare the solutions to the initial value problem and have that $$\Phi(t) = \Psi(t) (\Psi(t_0))^{-1} $$

## Matrix Exponential

We consider the the scalar initial value problem $$x' = ax\qquad x(0) = x_0$$where $a$ is a constant, is $$x = x_0\exp(at)$$Now considering the corresponding initial value problem for an $n\times n$ system, namely $$x' = Ax \qquad x(0) = x_0$$
where $A$ is a constant matrix. Applying what we have seen we have that $$x  = \Phi(t) x_0$$ where $\Phi(0) =I$. We also have that $\Phi' = A \Phi$. So it feels like it has a exponential character. 

We look at the definition of the matrix exponential of $At$, the $$\exp(At) = \sum_{n = 0}^\infty \frac{A^n t^n}{n!}$$By differentiating the series term by term, we obtain that $$\frac{d}{dt}\exp(At) = A \exp(At)$$further, when $t = 0$, $\exp(At)$ satisfies the initial condition $$\exp(At)\biggr\rvert_{t = 0} = I$$The fundamental matrix $\Phi$ satisfies the same initial value problem as $\exp(At)$. if we extend the existence and uniqueness of system of differential equations, to existence and uniqueness for matrix differential equations, we conclude $\exp(At)$ is the fundamental matrix $\Phi$. 

Then we can the solution to $x' = Ax$, with $x(0) =x_0$, is $$x = \exp(At) x_0$$
If we look to the system $$x' = Ax$$where $A$ is a constant matrix. Then we can look at the Jordan normal form with $A= PJP^{-1}$, where $P$ is a matrix constituting of the generalised eigenvectors of $A$. We can consider a change in variable $$x = Py$$Then we have that $$Py' = APy$$
which is equivalent to $$y = P^{-1}AP y = Jy$$This last matrix is manageable to exponentiate, we name $$Q(t) = \exp(Jt)$$we have that the fundamental matrix $\Psi$ can be found from $Q$ by $$\Psi = PQ$$
