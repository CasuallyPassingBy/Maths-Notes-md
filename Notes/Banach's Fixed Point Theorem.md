---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Complete Metric Spaces]], [[Continuity on Metric Spaces#Lipschitz Continuity|Lipschitz Continuity]]
Let $\phi:X\to X$ it is called a _contraction_ if there exists $\alpha\in (0,1)$ such that

$$ d(\phi(x), \phi(y)) \le \alpha d(x, y) \qquad \forall x, y\in X $$

This means it is a Lipschitz continuous function with the added constraint that the Lipschitz constant is in $(0,1)$

A point $x^* \in X$ it is called a *___fixed point of $\phi$, $\phi: X\to X$_ if $\phi(x^*) = x^*$

We can also denote $\phi^k = \underbrace{\phi \circ \phi \circ \dots\circ\phi}_{k \text{ times}}$ with $k \in \Bbb N^+$, and $\phi^0 = \text{id}_X$

### Banach’s Fixed Point Theorem

Let $X$ be a nonempty complete metric space, and let $\phi:X \to X$ be a contraction. Then

- $\phi$ has a unique fixed point $x^*$
    
- For any $x_0 \in X$, the sequence $(\phi^k(x_0))_{k \in \Bbb N}$ converges to $x_0$ and and it satisfies that
    
    $$ d(\phi^k(x_0), x^*) \le \frac{\alpha^k}{1-\alpha}d(\phi(x_0), x_0) $$
    
    where $\alpha\in (0,1)$ is the Lipschitz constant
    

This theorem actually, tells you how to find the fixed point. We pick a point $x_0 \in X$, then we construct the sequence $(\phi^k(x_0))_{k \in \Bbb N}$ and we can approximate the error, using the second bullet point. This method is a _********method of successive approximations********_.

We get a corollary: let $X$ be a nonempty complete metric space and $\phi: X\to X$ be a function. If therze’s $k \in \Bbb N$ such that $\phi^k : X \to X$ is a contraction, then $\phi$ has a unique fixed point

Let $f: \Bbb R \to \Bbb R$ be continuously differentiable on $\Bbb R$ and $|f'(x)| \le M<1$ for all $x\in \Bbb R$, then $f$ is a contraction

Let $f:[a, b]\to \Bbb R$ be continuously differentiable on $[a,b]$ and such that $f(a) < 0 <f(b)$ and $f'>0$. Then there’s a unique $x^* \in [a,b]$ such that $x^*$ that can be found using the method of successive approximations. We use a function $\phi_\lambda(x) = x-\lambda f(x)$, and if we find $\lambda>0$ such that $\phi_\lambda$ is a contraction, then we can find the unique $0$ of $f$. We can find $\lambda$ such that $M$ is the maxium of $f'$ on $[a, b]$, then $\lambda = 1/2M$, we make sure $\phi_\lambda$ is a contraction. This method is used in Numerical Analysis, in particular in the algorithm called: [[Fixed Point Iteration]]

Let $X$ be a nonempty [[Compactness in Metric Spaces|compact set]], and $\phi: X\to X$, such that

$$ d(\phi(x), \phi(y)) < d(x, y) \qquad x\ne y $$

This function is uniformly continuous, and has a unique fixed point 