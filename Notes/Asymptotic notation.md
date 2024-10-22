---
tags:
  - AlgorithmsAndDataStructures
---
Subjects: [[Algorithms and Data Structures]]
Links: [[limsup and liminf]]

There are a lot of asymptotic notation, telling us how a function grows in the long run
# $\Theta$-notation

For a given $g(n)$ we denote by $\Theta(g(n))$ the *set of functions*: $$\Theta(g(n)) = \{f(n) \mid \exists c_1, c_2 >0 \exists n_0 \in \Bbb N \forall n \ge  n_0 [c_1 g(n) \le f(n) \le c_2 g(n)]\}$$
A function $f(n)$ belongs to the set $\Theta(g(n))$ if there exists positive constants $c_1$ and $c_2$ such that it can be "sandwiched" between $c_1 g(n)$ and $c_2g(n)$, for sufficiently large $n$. Because $\Theta(g(n))$ is a set, it would be the correct thing to do is to write $f(n) \in \Theta(g(n))$, to indicate that $f(n)$ is a member of $\Theta(g(n))$. We will write $f(n) = \Theta(g(n))$, since it will be more confortable. 

We see that by the definition, for all $n \ge n_0$ the function $f(n)$ is equal to $g(n)$ to within a constant factor. We say that $g(n)$ is an *asymptotically tight bound* for $f(n)$. 

We actually see we can have an alternative definitions, we say that $f(n) = \Theta(g(n))$ iff $$\limsup_{n \to \infty} \frac{f(n)}{g(n)} <\infty \qquad \text{and} \qquad \liminf_{n \to \infty} \frac{f(n)}{g(n)} > 0$$
The definition of $\Theta(g(n))$ requires that every $f \in \Theta(g(n))$ be *asymptotically nonnegative*, meaning for sufficiently large $n$ $f(n)$ is nonnegative. To solve we can just consider the absolute value of the function. Consequently, the function $g(n)$ itself must be asymptotically nonnegative, or else $\Theta(g(n))$ is empty. 

We use another slight abuse of notation considering $\Theta(1)$ as the $0$th degree polynomial, since it doesn't show which variable goes to infinity.

Doing some algebra, we see that if $f(n) = \Theta(g(n))$, then $g(n) = \Theta(f(n))$. Similarly, $f(n) = \Theta(f(n))$. Lastly we got that if $f(n) = \Theta(g(n))$ and $g(n) = \Theta(h(n))$, then $f(n) = \Theta(h(n))$. This behaves is an equivalence relation.

# $O$-notation

When we have only an *asymptotic upper bound*, we use $O$-notation. For a given function $g(n)$, we denote by $O(g(n))$ the set of functions $$ O(g(n)) = \{f(n) \mid \exists c > 0 \exists n_0 \in \Bbb N \forall n \ge n_0[0 \le f(n) \le cg(n)]\}$$
we use $O$-notation to give an upper bound on a function, to within a constant factor. We write $O(g(n))$ to indicate that a  function $f(n)$ is a member of $O(g(n))$. We see that $f(n) = \Theta(g(n))$, implies that $f(n) = O(g(n))$. We can write this as $\Theta(g(n)) \subseteq O(g(n))$. 

Similarly as we had for $\Theta(g(n))$, we can use limits to give an alternate definition, $f(n) = O(g(n))$ iff $$\limsup_{n \to \infty} \frac{f(n)}{g(n)} < \infty$$
$O$-notation is not necessarily a tight bound. 

We might be interested in what happens when $g(n) = O(f(n))$ and $f(n) = O(g(n))$. When this happens we see that we are bounding $f$ by below and above by $g$, getting that $f(n) = \Theta(g(n))$

Doing some algebra, we see that $f(n) = O(f(n))$. We got that if $f(n) = O(g(n))$ and $g(n) = O(h(n))$, then $f(n) = O(h(n))$. Adding the last point, we see that $O$ is an order relation on the space of asymptotically nonnegative functions modulo $\Theta$



# $\Omega$-notation

Just as $O$-notation provides an asymptotic upper bound on a function $\Omega$-notation provides an *asymptotic lower bound*. For a given function $g(n)$, we denote by $\Omega(g(n))$ the set of functions $$\Omega(g(n)) = \{f(n) \mid \exists c > 0 \exists n_0 \in \Bbb N \forall n \ge n_0[0 \le cg(n) \le f(n)]\}$$
We see a nice equivalence that $f(n) = O(g(n))$ iff $g(n) = \Omega(f(n))$

We also see that $f(n) = \Omega(g(n))$, iff $$\liminf_{n \to \infty} \frac{f(n)}{g(n)} > 0$$
**Th:** For any two function $f(n)$ and $g(n)$, we have that $f(n) = \Theta(g(n))$ iff $f(n) = O(g(n))$ and $f(n) = \Omega(g(n))$.

Which can be thought of as the inverse ordering given by $O$

# $o$-notation

The asymptotic upper bound provided by $O$-notation may or may not be asymptotically tight. We use $o$-notation to denote an upper bound that is not asymptotically tight. We formally define $o(g(n))$ as the set $$o(g(n)) =\{f(n) \mid \forall c > 0 \exists n_0 \in \Bbb N \forall n \ge n_0[0 \le f(n) < cg(n)]\}$$
The definitions of $O$-notation and $o$-notation are similar. If we look at the the limit equivalence we see that $f(n) = o(g(n))$ iff $$\lim_{n \to\infty} \frac{f(n)}{g(n)} = 0$$
Our choice of notation is not arbitrary, we see that $f(n) \ne o(f(n))$, and if $f(n) = o(g(n))$ and $g(n) = o(h(n))$, then $f(n) = o(h(n))$. Meaning that it behaves like a strict ordering, of $O$. We also have that $o(g(n)) \subseteq O(g(n))$

# $\omega$-notation

We use $\omega$-notation to denote a lower bound that is not asymptotically tight. One way to define it is by $$f(n) = \omega(g(n))  \iff g(n) = o(f(n))$$
Formally, we define $\omega(g(n))$ as the set $$\omega(g(n)) = \{f(n) \mid \forall c > 0 \exists n_0 \in \Bbb N \forall n \ge n_0[0 \le cg(n) < f(n)]\}$$
we see that is equivalent that $f(n) = \omega(g(n))$ iff $$\lim_{n \to \infty} \frac{f(n)}{g(n)} = \infty$$if the limit exists. We see that $f(n) \ne \omega(f(n))$, and of $f(n) = \omega(g(n))$ and $g(n) = \omega(h(n))$, then $f(n) = \omega(h(n))$. Then we see that $\omega$-notation is the strict ordering associated with $\Omega$-notation. We also have that $\omega(g(n)) \subseteq \Omega(g(n))$. 

We have a similar relation as we have for $O$ and $\Omega$-notations, with $f(n) = o(g(n))$ iff $g(n) = \omega(f(n))$

# Common functions

### Polynomials
Given a nonnegative integer $d$, a polynomial in $n$ of degree $d$ is a function $p(n)$ of the form $$p(n) = \sum_{k = 0}^d a_k n^k$$where the constants $a_0, a_1, \dots, a_d$ are the *coefficients* of the polynomial and $a_d\ne 0$. A polynomials is asymptotically positive iff $a_d >0$. We have a nice relations: 
- if $k \ge d$ then $p(n) = O(n^k)$
- if $k \le d$ then $p(n) = \Omega(n^k)$
- if $k = d$ then $p(n) = \Theta(n^k)$
- if $k > d$ then $p(n) = o(n^k)$
- if $k < d$ then $p(n) = \omega(n^k)$

We say that $f(n)$ is *polynomially bounded* if $f(n) = O(n^k)$ for some constant $k$

### Logarithms
We say that a function $f(n)$ is *polylogarithmically bounded* if $f(n) = O((\log n)^k)$ for some constant $k$. We have the nice relation that $$(\log n)^b = o(n^a)$$ for any constant $a>0$. 

### Factorials
A weak upper bound on the factorial function is $n! \le n^n$, since each of the $n$ terms in the factorial product is at most $n$. *Stirling's approximation formula,* $$n! = \sqrt{2\pi n} \left(\frac ne\right)^n \left(1+ \Theta\left(\frac1n\right)\right) $$
We have that:
- $n! = o(n^n)$
- $n! = \omega(2^n)$
- $\log n! = \Theta(n \log n)$

### Iterated logarithm function
We use the notation $\log^* n$ to denote the iterated logarithm. First we need a bit of notation, let $f(n) = \log n$, then we define $f^{(i+1)}(n) = f(f^{(i)}(n)$, and with the base case that $f^{(0)}(n) = n$. The only thing we need to check before trying to compute $f^{(i)}(n)$ is to see that $f^{(i-1)}(n) > 0$. 

We define the iterated logarithm function as $$\log^* n:= \{i \in \Bbb N \mid \log^{(i)} n \le 1\}$$