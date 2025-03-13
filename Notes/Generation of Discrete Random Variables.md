---
tags:
  - StochasticSimulation
---
Subjects: [[Stochastic Simulation]]
Links: [[Pseudo-random number generator]], [[Discrete Distributions]]

Since we can generate a random number $U \sim \text{Unif}(0, 1)$, a natural progression is to transform it into another continuous random variable. A counterpart to this, is to transform a $U \sim \text{Unif}(0, 1)$ [[Generation of Continuous Random Variables|into continuous random variables]]. There are different methods:

# Inversion Method

Let $X$ be a discrete random variable, then we have that $f_X(x_i) = p_i$ for $i \in \Bbb N$, and $\sum_{i = 0}^\infty p_i = 1$. We can generate a $U \sim \text{Unif}(0, 1)$, then: $$X = 
\begin{cases} 
x_0 & U < p_0 \\
x_0 & p_0 \le U<  p_0 + p_1 \\
\vdots  \\
x_i & \sum_{j < i} p_i \le U < \sum_{j \le i} p_i \\
\vdots
\end{cases}$$
If there are a finite amount of possible values we can write the information inside of a dictionary. 
```python

def discrete_inversion_sampling(random_variable_probabilities:dict[float, float]) -> float:
	list_of_values_probabilities = list(random_variable_probabilities.items())
	list_of_values_probabilities = sorted(list_of_values_probabilities, key = lambda x: x[0])
	u = np.random.uniform()
	total_probability = 0
	
	for value, probability in list_of_values_probabilities:
		if total_probability <= u < total_probability + probability:
			return value
	
		total_probability += probability

random_variable_probabilities = {
	0 : 0.33,
	1 : 0.33,
	2 : 0.33,
	3 : 0.01
}

coinflip = lambda : discrete_inversion_sampling(random_variable_probabilities)

print([coinflip() for _ in range(20)])

```

# Specific Distributions

### Bernoulli
With this method we can generate a Bernoulli random variable with parameter $p$. 

```python
def bernoulli_sampling(p:float) -> int:
	u = np.random.uniform()
	if p <= u:
		return 1
	return 0
```

### Binomial

Now we can generate a Binomial random variable with parameters $n$ and $p$: 

```python
def binomial_sampling(n:int, p:float) -> int:
	total = 0
	for _ in range(n)
		total += bernoulli_sampling(p)
	return total
```

There's a faster way to generate a $\text{Bernoulli}(n, p)$: 

```python
def fast_binimial_sampling(n:int, p:float) -> int:
	u = np.random.uniform()
	c = p/(1-p)
	F = (1-p)**n
	pr = (1-p)**n
	for i in range(0, n):
		if u < F:
			return i
		pr *= c*(n-i)/(i+1)
		F += pr
	return n
```

### Poisson

To generate a Poisson random variable we get the algorithm:

```python
def poisson_sampling(mean):
	u = np.random.uniform()
	i = 0
	p = np.exp(-mean)
	F = p
	while True:
		if u < F:
			return 0
		p = mean*p/(i+1)
		F = F+p
		i += 1
```


### Geometric

We can get a nice algorithm to get a $X \sim \text{Geo}(p)$:

```python
def geometric_sampling(p):
	u = np.random.uniform()
	return np.floor(np.log(1-u)/np.log(1-p)) +1
```


### Negative Binomial

Now we can generate $\text{Neg Bin}(n, p)$ with this algorithm:

```python
def negative_binommial_sampling(n:int, p):
	total = 0
	for _ in range(n):
		total += geometric_sampling(p)
	return total
```