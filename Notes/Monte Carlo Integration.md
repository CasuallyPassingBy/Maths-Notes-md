---
tags:
  - StochasticSimulation
  - NumericalAnalysis
---
Subjects: [[Stochastic Simulation]], [[Numerical Analysis]]
Links: [[Pseudo-random number generator]], [[Numerical Integration]]

We would like to approximate the integral $$I = \int_a^b h(x)\, dx.$$For $g(x) = h(x)(b-a)$ and $f(x)$ be a pdf of $(a, b)$, we have that $$I = \int_a^b h(x)\, dx = \int_a^b g(x) f(x)\, dx = E_f(g(x)).$$We can generate a sample of $X$ with density $f \sim \text{Unif}(a, b)$ and approximate this integral by $$h^* = \frac1n \sum_{i = 1}^n g(x_i).$$
Monte Carlo integration uses random sampling of a function to estimate the value of its integral. $$I = \int_a^b f(x)\, dx.$$We get that the Monte Carlo estimator is equal to $$F^N = (b-a) \frac1n \sum_{i = 1}^N f(x_i).$$
```python
import micropip 
await micropip.install('numpy')
await micropip.install('matplotlib')
import numpy as np
import matplotlib.pyplot as plt

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

# x_values = np.linspace(0, 5, 100)
# y_values = [f(x) for x in x_values]
# plt.plot(x_values, y_values, c = 'blue')
# plt.grid(True)
# plt.show()
```
[[[[[[]()]()]()]()]()]()