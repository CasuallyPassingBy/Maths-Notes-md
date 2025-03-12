---
tags:
  - StochasticSimulation
---
Subjects: [[Stochastic Simulation]]
Links: [[Pseudo-random number generator]], [[Goodness of Fit Tests]]

In general there is a lot of code in this section, but we will need this libraries to run everything locally:

```python
import micropip 
await micropip.install('numpy') 
import numpy as np
await micropip.install('scipy')
import scipy.stats as stats


sample = [0, 1, 1, 2, 3, 5, 8, 3, 1, 4, 5, 9, 4, 3, 7, 0, 7, 7, 4, 1, 5, 6, 1, 7, 8, 5, 3, 8, 1, 9, 0, 9, 9, 8, 7, 5, 2, 7, 9, 6, 5, 1, 6, 7, 3, 0, 3, 3, 6, 9, 5, 4, 9, 3, 2, 5, 7, 2, 9, 1, 0]
```

# Goodness of Fit Tests

This kind of tests help us determine that these are uniformly distributed samples
## $\chi^2$-Test

```python
def chi_squared_test_uniformity(sample):
	sample = np.array(sample)
	bins = np.max(sample) + 1
	hist, _ = np.histogram(sample, bins = np.arange(bins + 1))
	expected = np.full(bins, hist.sum() / bins)
	chi_stat, p_value = stats.chisquare(hist, expected)
	print(f"Chi-Square Test: p-value = {p_value:.4f}")
	if p_value > 0.05:
		print("Pass: No strong evidence of non-uniformity.")
	else:
		print("Fail: Evidence suggests non-uniformity.")

chi_squared_test_uniformity(sample)
```

## Kolmogorov-Smirnov Test

```python
def kolmogorov_smirnov_test_uniformity(normalized_sample):
	ks_stat, p_value = stats.ks_1samp(normalized_sample, stats.uniform.cdf)
	print(f"KS Test: p-value = {p_value:.4f}")
	
	if p_value > 0.05:
		print("Pass: No strong evidence against uniformity.")
	
	else:
		print("Fail: Evidence suggests the distribution is not uniform.")

maximum = max(sample) + 1 
normalized_sample = [x/maximum for x in sample]
kolmogorov_smirnov_test_uniformity(normalized_sample)
```

# Independece Tests

This kind of tests help us to test for randomness

## Gaps Tests
