---
tags:
  - NumericalAnalysis
---
Subjects: [[Numerical Analysis]]
Links: [[Solutions of Equations of One Variable]]

Suppose $f \in \cal C^2[a,b]$. Let $p_0 \in [a,b]$ be an approximation of $p$ such that $f'(p_0) \ne 0$ and ${|p - p_0|}$ is “small”. Then we can use a Taylor approximation about $p_0$ and evaluated at $p$. If we neglect the term with $|p -p _0|^2$ since it is is so small, then we get that

$$ 0= f(p) \approx f(p_0) +(p-p_0)f'(p_0) $$

solving for $p$, we get that

$$ p \approx p_0 -\frac{f(p_0)}{f'(p_0)} $$

Then we can define Newton’s Method, as the following

$$ p_{n+1} = p_n - \frac{f(p_n)}{f'(p_n)} \quad \text{for }n \in \Bbb N $$

### Newton’s Method Code

```julia
function newton_method(f, f_prime, x0, tol=1e-6, max_iter=1000)
    # Initialize the iteration counter and the initial approximation
    x_current = x0
    
    for i in 1:max_iter
        f_val = f(x_current)       # Evaluate the function
        f_prime_val = f_prime(x_current)  # Evaluate the derivative
        
				# Check if the derivative is close to zero
        if abs(f_prime_val) < tol
						println("Derivative close to zero. Newton's method cannot proceed.")
            return x_current
        end
				# Update the approximation using Newton's method
        x_next = x_current - f_val / f_prime_val

        # Check for convergence
        if abs(x_next - x_current) < tol # we can change this inequality for any of the other 3, 
            return x_next
        end
				
        x_current = x_next
    end
    
    println("Did not converge within the maximum iterations.")
    return x_current
end
```

### Convergence Theorem

Let $f \in \mathcal C^2[a,b]$. If $p \in (a,b)$ such that $f(p) = 0$ and $f'(p) = 0$, then there exists a $\delta >0$ such that Newton’s method generates a sequence $(p_n)_{n \in \Bbb N}$ converging to $p$ for any initial approximation $p_0 \in [p - \delta, p +\delta]$

The idea to find this $\delta$ is that if we consider $g(x) = x - \frac{f(x)}{f'(x)}$, then $g'(x) = \frac{f(x)f''(x)}{f'(x)^2}$. Then if $g(p) = p$, and $g'(p) = 0$, this means that $p$ is a super attractive fixed point of $g$. Meaning we if that we can find $\delta >0$, such that it is a contraction on that interval, and thus it converges. But in practice it just means to have a reasonable first guess of the solution, or look it up first with bisection on $f$, and consequently we get closer to the region where $g$ is contraction.

We can calculate the error by using the Taylor’s Expansion, with the hypothesis of the theorem and with $\| f''\|_\infty \le M$

$$ |p _{n+1} - p| = \frac{M}{2|f'(p_n)|}|p - p_n|^2 $$This method can be modified in a bit of ways to get a different results:
- [[Secant Method]]
- [[Method of False Position]]