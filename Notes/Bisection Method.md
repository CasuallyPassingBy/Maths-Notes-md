---
tags:
  - NumericalAnalysis
---
Subjects: [[Numerical Analysis]]
Links: [[Solutions of Equations of One Variable]]

The first technique, based on the [[Intermediate Value Theorem in R|IVT]], is called _********Bisection********_ or _**Binary Search method**_

Suppose $f$ is a continuous function defined on the interval $[a, b]$, with $f(a)$ and $f(b)$ of opposite sign. The Intermediate Value Theorem implies that a number $p$ exists in $(a, b)$ with $f(p) = 0$ Although the procedure will work when there is more than one root in the interval $(a, b)$, we assume for simplicity that the root in this interval is unique. The method calls for a repeated halving (or bisecting) of subintervals of $[a, b]$ and, at each step, locating the half containing p.

To begin, set $a_1 = a$ and $b_1 = b$ and let $p_1$ be the midpoint of $[a, b]$, that is.$$ p_1 = a_1 + \frac{b_1 - a_1}{2} = \frac{a_1 + b_1}{2} $$

- If $f(p_1 ) = 0$, then $p = p_1$, and we are done
- If $f(p_1) \ne 0$, then $f(p_1)$ must have the same sign as $f(a_1)$ or $f(b_1)$
    - If $f(p_1)$ and $f(a_1)$ have the same sign, $p \in (p_1, b_1)$. Set $a_2 = p_1$ and $b_2 = b_1$
    - If $f(p_1)$ and $f(b_1)$ have the same sign, $p \in (a_1, p_1)$. Set $a_2 = a_1$ and $b_2 = p_1$

then we reapply this process

### Bisection Code

```python
def bisection(f, a:float, b:float, tolerance:float = 1e-6, max_iterations:int = 1_000):
	def sign(x):
		return (x> 0) - (x < 0)
	if sign(f(a))* sign(f(b)) > 0:
		raise Exception(f'The endpoints {a} and {b} must have different signs when evaluated by the function')
		
	iteration = 0
	midpoint = (a+b)/2
	
	while (abs(f(midpoint)) > tolerance) and (iteration < max_iterations):
		midpoint = (a+b)/2
		fp = f(midpoint)
		if fp == 0 or (b-a)/2 < tolerance:
			return midpoint
		elif sign(fp) * sign(f(a)) < 0:
			b = midpoint
		else:
			a = midpoint
		iteration += 1
	return midpoint	

f = lambda x: x*x - 2
a = 1
b = 2
print(bisection(f, a, b, tolerance = 1e-7))
```


We have multiple criterion for stopping the algorithm given a tolerance $\varepsilon$, while generating $p_1, \dots, p_N$ until one of the condition is met

$$ \begin{align} |p_N - p_{N-1}| &< \varepsilon \\ \frac{|p_N - p_{N-1}|}{|p_N|} &< \varepsilon \quad p_N \ne 0\\

|f(p_n)| &< \varepsilon \end{align} $$

Each of this criterion for stopping can be problematic, since $f$ can be problematic. We can have that in certain cases $(p_n)_{n \in \Bbb N}$ is a pseudo Cauchy sequence, that diverges. We can have that $f(p)$ be really small while being nowhere near the actual $0$. The second inequality is the best stopping criterion to apply because it comes closest to testing relative error.

********Th:******** Suppose that $f \in {\cal C}[a,b]$ and $f(a) f(b) <0$. The Bisection method generates a sequence $(p_n)_{n \in \Bbb N}$ approximating a zero $p$ of $f$ with $$ |p_n - p| \le \frac{b-a}{2^n} $$
Meaning the sequence $p_n = p + O(2^{-n})$. This is quite the loose bound for most cases, we can find a formula to find the least $n$, such that given any tolerance $\varepsilon$, we get that if$$ \log_2\left(\frac{b-a}{\varepsilon}\right) < n $$so the least $n$ that satisfies that if the ceiling of that, or the ceiling of that $+1$. This allows us to have more of an idea of how many steps are necessary for the desired precision of the input. Meaning that $|p_n - p| < \varepsilon$, we can still want that $|f(p_n)| < \varepsilon$, and this is much harder to control without info of the function.