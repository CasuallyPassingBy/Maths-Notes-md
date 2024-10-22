---
tags:
  - NumericalAnalysis
---
Subjects: [[Numerical Analysis]]
Links: [[Solutions of Equations of One Variable]]

The main problem of using Newton’s method is the need of the derivative of $f$ at each approximation. Sometimes $f'(x)$ can be more complicated to calculate than $f(x)$. If we look at the definition of derivative, we get it as

$$ f(p_{n}) = \lim_{x \to p_{n}} \frac{f(x) -f(p_{n})}{x - p_{n}} $$

If $p_{n-1}$ is close to $p_{n}$, then

$$ f'(p_{n}) \approx \frac{f(p_{n}) -f(p_{n-1})}{p_{n} - p_{n-1}} $$

Using this approximation for $f'(p_{n})$ to Newton’s Method, we get

$$ p_{n+1} = p_n -\frac{f(p_n)(p_n -p_{n-1})}{(f(p_n) - f(p_{n-1}))} $$

This is called the **_Secant method_**

### Secant Method Code

```julia
function secant_method(f, x0, x1, tol = 1e-6, max_iter = 1000)
    # Initialize the iteration counter and the initial approximations
    x_prev = x0
    x_current = x1
    
    for iter in  1:max_iter
        f_prev = f(x_prev)       # Evaluate the function at the previous approximation
        f_current = f(x_current) # Evaluate the function at the current approximation
        
        # Check for convergence
        if abs(x_prev - x_current) < tol  # this can change to any of the 3 inqualites to check for convergence
            return x_current
        end
        
        # Check if the difference is close to zero
        if abs(x_current - x_prev) < tol
            println("Difference between approximations close to zero. Secant method cannot proceed.")
            return x_current
        end
        
        # Update the approximation using the secant method
        x_next = x_current - f_current * (x_current - x_prev) / (f_current - f_prev)
        x_prev = x_current
        x_current = x_next
    end
    
    println("Did not converge within the maximum iterations.")
    return x_current
end
```

This method is generally slower than Newton’s Method, but also generally cheaper to compute. This method and Newton’s Method is used to refine an answer obtained by another technique, since they already need quite a good approximations but generally converges rapidly.