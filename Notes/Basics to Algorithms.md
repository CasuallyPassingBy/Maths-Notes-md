---
tags:
  - "#AlgorithmsAndDataStructures"
---
Subjects: [[Algorithms and Data Structures]]
Links: [[Asymptotic notation]]

# Insertion Sort

Our first algorithm, insertion sort, solves the *sorting problem*:

*Input:* A sequence of $n$ numbers $\langle a_1, a_2, \dots, a_n\rangle$
*Output:* A permutation $\langle a_1', a_2', \dots, a_n'\rangle$ of the input of sequence such that $a_1' \le a_2' \le \cdots \le a_n'$ 

The numbers we wish to sort are also known as the *keys*. 

*Insertion sort* is an efficient algorithm for sorting a small number of elements, or mostly sorted lists. The way insertion sort works is by expanding an ordered sub-list by finding where on the ordered sub-list the next elements place, and slowly expanding it.

The algorithms sorts the input numbers in *in place*: it rearranges the numbers within the array $A$, with at most a constant number of them stored outside the array at any time. 


```cpp 
#include <iostream>
#include <vector>

void insertion_sort(std::vector<int>& arr){
	int n = arr.size();
	for (size_t i = 1; i < n; ++i)
	{
		int key = arr[i];
		int j = i -1;

		while (j >= 0 && arr[j] > key) {
			arr[j+1] = arr[j];
			--j;
		}
		arr[j+1] = key;
	}
}

int main(){
	std::vector<int> arr = {12, 11, 13, 5 ,6};
	insertion_sort(arr);

	std::cout << "sorted array: ";
	for (int i = 0; i < arr.size(); i++)
		std::cout << arr[i] << ' ';
	std::cout << std::endl;
	// output on console: sorted array: 5 6 11 12 13 
	return 0;
}
```
### Loop invariants and the correctness of insertion sort

We use loop invariants to help us understand why an algorithm is correct. We must show three things about a loop invariant:
- *Initialisation:* It is true prior to the first iteration of the loop
- *Maintenance:* If it is true before an iteration of the loop, it remains true before the next iteration
- *Termination:* when the loop terminates, the invariant gives us a useful property that helps show that the algorithm is correct.

This is similar to finite mathematical induction.

# Divide-and-conquer approach

Many useful algorithms are *recursive* in structure: to solve a given problem they call themselves recursively one or more times to deal with closely related sub-problems. 

These  algorithms typically follow a *divide-and-conquer* approach: they break the problem into several sub-problems that are similar to the original problem but smaller in size, solve the sub-problems recursively, and then combine these solutions to create a solution to the original problem

The divide-and-conquer are involves three steps at each level of recursion:
- *Divide* the problem into a number of sub-problems that are smaller instances of the same problem
- *Conquer* the sub-problems by solving them recursively. If the problem sizes are small enough, however just solve the sub-problems in a straightforward manner
- *Combine* the solutions to the subproblem into the solution for the original problem

> These are the basic guidelines for many important algorithms in CS

#### Merge Sort

The *merge sort* algorithm closely follows the divide-and-conquer paradigm:
- *Divide:* Divide the $n$ element sequence to be sorted into two sequences of $n/2$ elements
- *Conquer:* Sort the two subsequences recursively using merge sort
- *Combine:* Merge the two sorted subsequences to produce the sorted answer
The recursion bottoms out when the sequence to be sorted has length $1$, which is already sorted. 

The key to Merge sort, is the merging of two sorted sequences to get another sorted sequence. We can call an auxiliary procedure $\verb|Merge|(A, p, q, r)$ where $A$ is an array, and $p, q, r$ are indices into the array such that $p \le q < r$. The procedure assumes that the subarrays $A[p, \dots, q]$ and $A[q+1, \dots, r]$ are sorted in ordered. It *merges* them to form a single sorted subarray that replaces the current $A[p, \dots, r]$. 

This $\verb|Merge|$ procedure takes time $\Theta(n)$, where $n = r-p+1$ is the total of elements being merged.

```cpp
#include <iostream>
#include <vector>

void Merge(std::vector<int>& A, int p, int q, int r)
{
	int n1 = q-p+1;
	int n2 = r-q;
	
	std::vector<int> L(n1);
	std::vector<int> R(n2);
	
	for (size_t i = 0; i < n1; ++i)
		L[i] = A[p+i];
	for (size_t i = 0; i <  n2; ++i)
		R[i] = A[q + i+1];
	int i = 0;
	int j = 0;
	int k = p;

	// We use a while loop to check we are in the arrays at the same time
	while (i < n1 && j < n2)
	{
		if (L[i] <= R[j])
		{
			A[k] = L[i];
			++i;
		}
		else
		{
			A[k] = R[j];
			++j;
		}
		++k;
	}
	// This is used when we still have items left on L
	while (i < n1)
	{
		A[k] = L[i];
		++i;
		++k;
	}
	// This is used when we still have items left on R
	while (j < n2)
	{
		A[k] = R[j];
		++j;
		++k;
	}
}
```

The procedure $\verb|Merge|$ as a subroutine in the merge sort algorithm. The $\verb|Merge_sort|(A, p, r)$ sorts the elements of the subarray $A[p, \dots, r]$ into two sub arrays $\lceil n/2\rceil$ elements, and $A[q+1, \dots, r]$ containing $\lfloor n/2 \rfloor$ elements

```cpp
void Merge_sort(std::vector<int>& A, int p, int r)
{
	if (p < r)
	{
		int q = (p+r)/2;
		Merge_sort(A, p, q); 
		Merge_sort(A, q+1, r);
		Merge(A, p, q, r);
	}
}

int main(){
	std::vector<int> arr = {12, 11, 13, 5 ,6};
	Merge_sort(arr, 0, arr.size()-1);

	std::cout << "sorted array: ";
	for (int i = 0; i < arr.size(); i++)
		std::cout << arr[i] << ' ';
	std::cout << std::endl;
	// output on console: sorted array: 5 6 11 12 13 
	return 0;
}

```

We will later prove that the time for merge sort in asymptotic notation is $\Theta(n \log n)$. 