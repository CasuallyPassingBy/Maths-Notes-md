---
tags:
  - NumericalAnalysis
---
Subjects: [[Numerical Analysis]]
Links: [[Solutions of Equations of One Variable]]

The number $p$ is a **fixed point** for a given function $g$ if $g(p) = p$

Given a root finding problem $f(p) =0$, we can define function $g$ with a fixed point at $p$, as

$$ g(x) = x +\lambda f(x) $$

for $\lambda \in \Bbb R$. Conversely, ik a function $g$ has a fixed point at $p$, then the function defined by

$$ f(x) = x- g(x) $$

has a zero at $p$

********Th:********
- If a function $g\in {\cal C}[a,b]$ and $\operatorname{Im} g \subseteq [a,b]$, then $g$ has at least one fixed point in $[a,b]$
- If, in addition, $g$ is Lipschitz continuous with a Lipschitz constant $k <1$, then there is exactly one fixed point in $[a,b]$.

### Fixed Point of Functional Iteration

```julia
function fixed_point_iteration(g, x0; tol=1e-6, max_iter=1000)
    # Initialize the iteration counter and the initial approximation
    x_current = x0
    
    while i in 1:max_iter
        x_next = g(x_current)  # Compute the next approximation
        # Check for convergence
        if abs(x_next - x_current) < tol
            return x_next
        end

        x_current = x_next  # Update the approximation
    end
		println("Did not converge within the maximum iterations.")
    return x_current
end
```

### Fixed Point Theorem

Let $g \in \cal C[a,b]$ be such that $\operatorname{Im} g \subseteq [a,b]$. Suppose that $g$ is Lipscitz continuous with Lipschitz constant $k <1$. Then for any $p_0 \in [a,b]$, the sequence defined by

$$ p_{n+1} = g(p_n) \quad n \in\Bbb N $$

converges to the unique fixed point $p$, in $[a,b]$

**********Cor:********** Let $g \in \cal C[a,b]$ be such that $\operatorname{Im} g \subseteq [a,b]$. Suppose that $g$ is Lipschitz continuous with Lipschitz constant $k <1$, then the bounds for the error involved in using $p_n$ to approximate $p$ are given by

$$ |p_n -p| \le k^n \max\{p_0-a, b-p_0\} $$

and

$$ |p_n -p| \le \frac{k^n}{1-k}|p_1 - p_0| \quad \text{for all } n \ge 1 $$

Meaning that $p_n = p + O(k^n)$. With this we can construct given a tolerance $\varepsilon >0$, we can construct, the least $n$ necessary to have a precision of $\varepsilon$. We have that

$$ \log_k\left( \frac{\varepsilon(1-k)}{|p_1-p_0|}\right) < n $$

We have a that if $g \in \cal C[a,b]$, with $|g'(p)| >1$, then there’s a $\delta>0$ such that if ${0<|p_0 - p| <\delta}$, then $|p_0 - p| < |p_1 -p|$. Thus, no matter how close the initial approximation $p_0$ is to $p$, the next iterate $p_1$ is farther away, so the fixed-point iteration does not converge if${p_0 \ne p}$. This is where the definition of unstable fixed points comes from

Similarly, let $g$ be continuously differentiable on some interval $(c,d)$ that contains the fixed point $p$ of $g$. Then if $|g'(p)| < 1$, then there’s a $\delta >0$, such that if $|p_0 -p|\le \delta$, then the fixed point iteration converges.