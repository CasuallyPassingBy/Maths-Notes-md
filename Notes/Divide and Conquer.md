---
tags:
  - AlgorithmsAndDataStructures
---
Subjects: [[Algorithms and Data Structures]]
Links: [[Basics to Algorithms]], [[Asymptotic notation]]

The divide-and-conquer are involves three steps at each level of recursion:
- *Divide* the problem into a number of sub-problems that are smaller instances of the same problem
- *Conquer* the sub-problems by solving them recursively. If the problem sizes are small enough, however just solve the sub-problems in a straightforward manner
- *Combine* the solutions to the subproblem into the solution for the original problem

When the subproblems are large enough to solve recursively, we call the *recursive case*. Once the subproblems become small enough we no longer recourse, we say that that the recursion "bottoms out" and we have gotten down to the *base case*. We still need to consider that solution to subproblems that are smaller instances of the same problem, we need to consider solving such subproblems as part of the combine step.

### Recurrences

Recurrences go hand in hand with the divide-and-conquer paradigm, because they gibe us a natural way to characterise the running times of divide-and-conquer algorithms. the worst-case running time $T(n)$ of the [[Basics to Algorithms#Merge Sort|Merge sort]] procedure by the recurrence $$T(n) = \begin{cases}\Theta(1) & n = 1 \\ 2 T(n/2) + \Theta(n) & n > 1\end{cases}$$
There are different methods for solving recurrences, that is obtaining asymptotic $\Theta$ or $O$ bounds on the solution:
- In the *substitution method*, we guess a bound and then use mathematical induction to prove out guess correct
- The *recursion-tree method* converts the recurrence into a tree whose nodes represent the costs incurred at various levels of the recursion. 
- The *master method* provides bounds for recurrences of the form $$T(n) = a T(n/b) + f(n)$$where $a\ge 1$ and $b>1$, and $f(n)$ is a given function.

# The maximum-subarray problem

The idea of the problem is that you are given stock, and the prediction of the stock market for $n$ days, we want to maximise profits. 

#### A brute-force solution
We can easily devise a brute-force solution to his problem: just try every possible pair of buy and sell dates in which the buy precedes the sell date. A period of $n$ days has $n \choose 2$  such pair of dates. ${n \choose 2} = \Theta(n^2)$, this approach would take $\Omega(n^2)$ time.

#### A transformation
We want to design an algorithm with on $o(n^2)$ running time. Instead of considering the array itself to know when sell, we instead look at the daily price change, where the change on day $i$ is the difference between the prices after $i-1$ and after day $i$. 

With this in mind we now want to find the nonempty, contiguous subarray of $A$ whose values have the largest sum. We call this contiguous subarray the *maximum subarray*. 

Although computing the cost of one subarray might take time proportional to the length of the subarray, when computing all $\Theta(n^2)$ subarrays, we can organise the computation so that each subarrays takes $O(1)$ time, given the values of previously computed subarray sums. This makes the brute-force solution takes $\Theta(n^2)$ time.

```cpp
#include <iostream>
#include <vector>
#include <tuple>

std::tuple<int, int, int> brute_force_finding_maximum_subarray(const std::vector<int>& A, const int low, const int high){
	int max_right, max_left;
	int max_sum = A[low];
	int sum;
	for(int i = low; i <= high; i++){
		sum = 0;
		for(int j = i; j <= high; j++){
			sum += A[j];
			if (sum > max_sum){
				max_sum = sum;
				max_left = i;
				max_right = j;
			}
		}	
	}
	return std::make_tuple(max_left, max_right, max_sum);
}
```

### Using Divide-and-Conquer

Suppose we want a maximum subarray of the subarray $A[low, \dots, high]$. Divide-and-conquer suggest that we divide the subarray into two subarrays of as equal size as possible That is we find the midpoint, say $mid$, of the subarray, and consider the subarrays $A[low,\dots, mid]$ and $A[mid +1, \dots, high]$. Any contiguous subarray $A[i, \dots, j]$ of $A[low, \dots, high]$ must lie in exactly one of the following places:
- entirely in the subarray $A[low, \dots, mid]$, so that $low \le i \le j \le mid$
- entirely in the subarray $A[mid+1, \dots, high]$, so that $mid+1\le i \le j \le high$
- crossing the midpoint, so that $low \le i \le mid < j \le high$

We can easily find a maximum subarray crossing the midpoint in time linear in the size of the subarray $A[low, \dots, high]$. This problem is easier since we have the restriction of the subarray passing through the middle. The way this type of array is constructed, is by two subarrays $A[i, \dots, mid]$ and $A[mid+1, \dots, j]$ and then combine them. 

```cpp
#include <iostream>
#include <vector>
#include <tuple>
#include <climits> //For INT_MIN

std::tuple<int, int, int> find_max_crossing_subarray(const std::vector<int>& A, const int low, const int mid , const int high)
{
	int max_left = mid;
	int max_right = mid +1;
	int sum = 0;
	
	int left_sum = INT_MIN;
	for(int i = mid; i>= low; i--){
		sum += A[i];
		if (sum > left_sum){
			left_sum = sum;
			max_left = i;
		}
	}

	sum = 0;
	int right_sum = INT_MIN;
	for(int j = mid+1; j <= high; j++){
		sum += A[j];
		if (sum > right_sum)
		{
			right_sum = sum;
			max_right = j;
		}
	}
	return std::make_tuple(max_left, max_right, left_sum + right_sum);
}

```

If we count up the amount of operations in this algorithm, then we find that the time would be linear with respect to the input size, meaning $\Theta(n)$. with a linear-time $\verb|find_max_crossing_subarray|$,we can write code for a divide-and-conquer algorithm to solve the maximum-subarray problem:

```cpp
std::tuple<int, int, int>find_maximum_subarray(const std::vector<int>A, const int low, const int high){
	if (high == low)
		return std::make_tuple(low, high, A[low]);
	int mid = (low + high)/2;
	
	auto [left_low, left_high, left_sum] = find_maximum_subarray(A, low, mid);
	auto [right_low, right_high, right_sum] = find_maximum_subarray(A, mid+1, high);
	auto [cross_low, cross_high, cross_sum] = find_max_crossing_subarray(A, low, mid, high);
	if (left_sum >= right_sum && left_sum >= cross_sum){
		return std::make_tuple([left_low, left_high, left_sum]);
	} else if (right_sum >= left_sum && right_sum >= cross_sum){
		return std::make_tuple(right_low, right_high, right_sum);
	} else {
		return std::make_tuple(cross_low, cross_high, cross_sum);
	}
}

int main(){
	std::vector<int> A = {-2, 1, -3, 4, -1, 2, 1, -5, 4};
	auto [low, high, sum] = find_maximum_subarray(A, 0, A.size()-1);
	std::cout <<  "Maximum subarray indices: (" << low << ", "<< high <<")\n";
	std::cout << "Maximum subarray sum: " << sum << std::endl;
	return 0;
}
```

If we analyse the performance we get the recurrence relation: $$T(n) = \begin{cases}\Theta(1) & n = 1 \\ 2 T(n/2) + \Theta(n) & n > 1\end{cases}$$We get that $T(n) = \Theta(n\log n)$. 

We can do even better, with a linear-time algorithm for the maximum-subarray problem. 

The way we do it is by keeping track of the maximum subarray of $A[1, \dots, j]$, extend the the answer to find the maximum subarray ending at the index $j+1$ by using the observation: a maximum subarray of $A[1, \dots, j+1]$ is either a maximum subarray of $A[1,\dots, j]$ or a subarray $A[i, \dots, j+1]$, for some $1\le i \le j+1$. 

```cpp
int KadaneAlgorithm(const std::vector<int>& A){
	int max_so_far = INT_MIN;
	int max_ending_here = 0;

	for(size_t i = 0; i < A.size(); ++i){
		max_ending_here = std::max(A[i], max_ending_here+A[i])
		max_so_far = std::max(max_so_far, max_ending_here)
	}
	return max_so_far;
}
```

# Strassen's algorithm for matrix multiplication

If  $A = (a_{ij})$ and $B= (b_{ij})$ are square $n\times n$ matrices, then in the product $C= A\cdot B$, we define the entry $c_{ij}$, for $i, j = 1,\dots n$, by $$c_{ij} = \sum_{k = 1}^n a_{ik}\cdot b_{kj}$$We must compute $n^2$ matrix entries, and each is the sum of $n$ values. The naive approach we can use the algorithm 

```cpp
#include <iostream>
#inclide <vector>

std::vector<float> MatrixMultiplication(std::vector<float> A, std::vecotr<float> B, int n){
	std::vector<float> C(A.size());
	for(size_t i =0; i < n; ++i){
		for (size_t j = 0; j < n; ++j){
			C[i * n + j] = 0;
			for(size_t k = 0; k < n; ++k){
				C[i * n + j] = A[i * n + j] * B[i * n + j]
			}
		}
	}
	return C;
}
```

We see that this algorithm takes $\Theta(n^3)$ time. 

### Strassen's method



