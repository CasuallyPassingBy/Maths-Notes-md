---
tags:
  - NumericalAnalysis
---
Subjects: [[Numerical Analysis]]
Links: [[Solutions of Equations of One Variable]], [[Fixed Point Iteration]], [[Newton's Method]], [[Horner and Müller Methods]], [[Secant Method]], [[Method of False Position]]

## Order of Convergence

Suppose $(p_n)_{n \in \Bbb N}$ is a sequence that converges to $p$, with $p_n \ne p$ for all $n$. If there are positive constants $\lambda$ and $\alpha$ such that

$$ \lim_{n \to \infty} \frac{|p_{n+1} -p|}{|p_n -p|^\alpha} = \lambda $$

then $(p_n)$ ************_converges to $p$ of order $\alpha$, with asymptotic error constant $\lambda$_

An iterative technique of $p_{n+1} = g(p_n)$ is said to be of order $\alpha$ if the sequence $(p_n)_{n \in \Bbb N}$ converges to the solution $p = g(p)$ of order $\alpha$

In general, a sequence with a order of convergence more rapidly than a sequence of lower order. The asymptotic constants affects the speed of convergence but not to the extent of the order. Two case are particularly important:

- If $\alpha = 1$ (and $\lambda <1$ ), the sequence is _**linearly convergent**_
- If $\alpha = 2$, the sequence is _**quadratically convergent_**

********Th:******** Let $g \in \cal C^1[a,b]$ be such that $\operatorname{Im} g \subseteq [a,b]$. Suppose that $\|g'\| \le k <1$. If $g'(p) \ne 0$, then for any $p_0 \ne p$ in $[a,b]$, the sequence

$$ p_{n+1} = g(p_n) \qquad \text{for }n \in \Bbb N $$

converges only linearly to the unique fixed point $p$ in $[a,b]$, we have that the asymptotic constant is $|g'(p)|$

********Th:******** Let $p$ be solution to $x = g(x)$. Suppose that $g'(p) = 0$ and $g''$ is continuous with ${\|g''\|_\infty < M}$ on an open interval $I$ containing $p$. Then there exists $\delta >0$ such that if ${p_0 \in [p -\delta, p +\delta]}$, the sequence $p_{n+1} = g(p_n)$ for $n \in \Bbb N$, converges at least quadratically to $p$. Moreover, for sufficiently large $n$,

$$ |p_{n+1} -p| < \frac{M}{2}|p_n -p|^2 $$

If $g''(p) = 0$, then it will be a higher order convergence. If $g''(p) \ne 0$, then it will be quadratic convergence with an asymptotic constant of $|g''(p)|/2$.

Given all of this we have that Newton’s Method is the simplest method with quadratic convegence

If we generalize this concept, to $g$, with $g^{(k)} (p) = 0$, for $0 \le k \le m$, for some $m$, and $\|g^{(m+1)}\| < M$ on an open interval $I$ containing $p$. Then there exists $\delta >0$ such that if ${p_0 \in [p -\delta, p +\delta]}$, the sequence $p_{n+1} = g(p_n)$ for $n \in \Bbb N$, converges at least with order $m +1$ to $p$. Moreover, for sufficiently large $n$,

$$ |p_{n+1} -p| < \frac{M}{(m+1)!}|p_n -p|^{m+1} $$

If $g^{(m+1)}(p) \ne 0$ then it will be a higher order of convergence. If $g^{(m+1)} (p) \ne 0$, then it will be of order $m+1$ with an asymptotic constant of $|g^{(m+1)}(p)| /(m+1)!$

## Multiple Roots

A solution $p$ of $f(x) = 0$ is a ********************zero of multiplicity******************** $m$ of $f$ it for $x \ne p$, we can write ${f(x) =(x-p)^m q(x)}$, where $\lim\limits_{x \to p} q(x) \ne 0$. We call _******simple******_ zeros those with multiplicitie of $1$

The function $f \in {\cal C}^1[a,b]$ has a simple zero at $p$ in $(a,b)$ iff $f(p) = 0$ but $f'(p)\ne 0$

In general, the function $f \in {\cal C}^m[a,b]$ has a zero multiplicity $m$ at $p \in (a,b)$ iff

$$ f^{(k)}(p) = 0 \quad \text{for }0 \le k <m \qquad\text{and}\qquad f^{(m)}(p) \ne 0 $$

The main problem with Newton’s Method is that it fails for non simple zeros of a function, then with that in mind we can consider a function $\mu(x)$, and supposing that $p$ is a zero of $f$ with multiplicity $m$, then

$$ \mu(x) = \frac{f(x)}{f'(x)} = (x-p) \frac{q(x)}{mq(x)+(x-p)q'(x)} $$

then $\mu$ has a simple zero at $p$, meaning we can apply Newton’s method to find $p$, getting

$$ g(x) = x -\frac{\mu(x)}{\mu'(x)} = x - \frac{f(x)f'(x)}{[f'(x)]^2 - f(x)f''(x)} $$

This is Modified Newton’s method, with $p_0$ being close to $p$, then

$$ p_{n+1} =p_n - \frac{f(p_n)f'(p_n)}{[f'(p_n)]^2 - f(p_n)f''(p_n)} $$

with this method we are assured to converge quadratically to $p$, regardless of the multiplicity of the zero of $f$

### Modified Newton’s Method Code

```julia
function modified_newton(f, f_prime, f_double_prime, x0, tol=1e-6, max_iter=1000)
    # Initialize the iteration counter and the initial approximation
    iter = 0
    x_current = x0
    
    while iter < max_iter
        f_val = f(x_current)       # Evaluate the function
        f_prime_val = f_prime(x_current)  # Evaluate the first derivative
        f_double_prime_val = f_double_prime(x_current)  # Evaluate the second derivative
        
        # Check for convergence
        if abs(f_val) < tol # This can be changed for different inequalities
            println("Converged after $iter iterations.")
            return x_current
        end
        
        # Check if the derivative is close to zero
        if abs(f_double_prime_val * f_prime_val + f_val) < tol
            println("The denominator is close to zero. Modified Newton's method cannot proceed.")
            return x_current
        end
        
        # Update the approximation using the modified Newton's method
        x_next = x_current - f_val * (f_prime_val / (f_double_prime_val * f_prime_val + f_val))
        
        x_current = x_next  # Update the approximation
        
        iter += 1
    end
    
    println("Did not converge within the maximum iterations.")
    return x_current
end
```

The problem of this can be the evalution of $f''$, but there’s also the probleme that there’s a lot of round off error, when substracting numbers that are close to zero and that provide a lot of round off error. So that’s an important thing to consider

We can also modify Newton’s Method such that it has convergence of order $3$, with $f(p) = 0$

$$ p_{n+1} = g(p_n) = p_n - \frac{f(p_n)}{f'(p_n)} -\frac{f''(p_n)}{2 f'(p_n)}\left(\frac{f(p_n)}{f'(p_n)}\right)^2 $$

since we have that $g'(p) = g''(p) = 0$, then by the theorem above, we know that this will converge in at least order $3$