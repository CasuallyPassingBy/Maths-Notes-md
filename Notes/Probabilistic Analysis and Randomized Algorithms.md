---
tags:
  - AlgorithmsAndDataStructures
---
Subjects: [[Algorithms and Data Structures]]
Links: [[Basics to Algorithms]], [[Asymptotic notation]], [[Random Variables]]

*Probabilistic analysis* is the use of probability in the analysis of problems. Most commonly, we use probabilistic analysis to analyse the running time of an algorithm. Sometimes we use it to analyse other quantities. We must have knowledge of the distribution of the inputs. Then we analyse the algorithm, computing the average-case running time, where we taje the average over the distribution of the possible inputs. Thus we are averaging the running time over all possible inputs. When reporting such a running time, we will refer to it as *average-case running time*.

We call an algorithm *randomised* if its behaviour is determined not only by its input but also by values produced by a *random-number generator*. We shall asume that we have at our disposal a random-number generator, but in practice most programming environments offer a *pseudo-random-number generator*: a deterministic algorithm returning numbers that "look" statistically random. 

When analysing the running time of a randomised algorithm, we take the expectation of the running time over the distribution of values returned by the random-number generator. We distinguish these algorithms from those in which the input is random by referring to the running time of a randomised algorithm as an *expected running time*. 

# Randomised algorithms

### Randomly permuting arrays

One common method is to assign each element $A[i]$ of the array a random priority $P[i]$, and then sort the elements of $A$ according to these priorities. We call thus procedure $\verb|Permute-by-sorting|$:

```cpp
#include <iostream>
#include <random>
#include <vector>
#include <algorithm>

void permute_by_sorting(std::vector<int>& A){
	int n = A.size();
	std::random_device rd; //Will be used to obtain a seed for the random number engine
	std::mt19937 gen(rd()); //Standard mersene_twister_engine seeded with rd()

	int lower_bound = 1;
	int upper_bound = n *n*n;

	std::uniform_int_distribution<> dis(lower_bound, upper_bound);

	std::vector<int> P(n);
	for(int i = 0, i < n; ++i){
		P[i] = dis(gen); //generates the random number
	}
	//Sort A using P as keys

	std::vector<std::pair<int, int>> PA(n);
	for(int i = 0; i < n; ++i){
		PA[i] = std::make_pair(P[i], A[i]);
	}

	std::sort(PA.begin(), PA.end());
 
	for(int = 0; i < n; ++i){
		A[i] = PA[i].second();
	}
}
```

It remains to prove that the procedure produces a *uniform random permutation*, that is, the procedure is equally likely to produce every permutation of the numbers $1$ through $n$.

**Lemma:** The procedure $\verb|Permute-by-sorting|$ produces a uniform permutation of the input, assuming that all priorities are distinct.

A better method for generating a random permutation is to permute the given array in place. The procedure $\verb|Randomize_in_place|$ does so in $O(n)$ time. In the $i$th iteration it chooses the $A[i]$ randomly from among elements $A[i]$ through $A[n]$. Subsequent to the $i$th iteration, $A[i]$ is never altered. 

```cpp
void randomize_in_place(std::vector<int>& A){
	int n = A.size();
	std::random_device rd;
	std::mt19937 gen(rd());
	int temp;
	for (size_t i = 0; i < n;++i){
		std::uniform_int_distribution<> dis(i,n-1);
		int j = dis(gen);
		int temp = A[i];
		A[i] = A[j];
		A[j] = temp;
	}
}
```

**Lemma:** The procedure $\verb|Randomize_in_place|$ computes a uniform random permutation.