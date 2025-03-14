---
tags:
  - StochasticSimulation
  - NumericalAnalysis
---
Subjects: [[Stochastic Simulation]], [[Numerical Analysis]]
Links: [[Pseudo-random number generator]], [[Numerical Integration]]


```python
import micropip 
await micropip.install('numpy')
import numpy as np

def bounded_monte_carlo_integration(integrated_function, a, b, N):
	total = 0
	for _ in range(N):
		x = a + (b - a) * np.random.uniform()
		total += integrated_function(x)
	total /= N
	total *= b - a
	return total

f = lambda x: -x ** 3 +5 * x +17

print(f'the estimated integral is {bounded_monte_carlo_integration(f, 0, 5, 100_000)}')
print('the real integral is -8.75')
```

