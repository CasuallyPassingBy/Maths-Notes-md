---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]], [[Natural Numbers]], [[Lambda Calculus]], [[Arithmetic of Natural Numbers]], [[Formalisms Equivalent to General Computation]]

Gödel defined a collection of number-theoretic functions $\Bbb N^k \to \Bbb N$ that, according to his intuition, represented all the computable functions. His definition was as follows:
- *Successor*. The function $\text s: \Bbb N \to\Bbb N$ given by $\text s(x) = x +1$ is computable.
- *Zero*. The function $\text z: \Bbb N^0 \to \Bbb N$ given by $z(\;) = 0$ is computable.
- *Projections.* the functions $\pi_l^n: \Bbb N^n \to \Bbb N$ given by $\pi_k^n(x_1,\dots, x_n) = x_k$, $1\le k\le n,$ are comutable.
- *Composition.* If $f: \Bbb N^k \to \Bbb N$ and $g_1, \dots, g_k:\Bbb N^n \to \Bbb N$ are computable, then so is the function $f\circ (g_1, \dots, g_n) : \Bbb N^n \to \Bbb N$ that an input $\overline x = (x_1,\dots, x_n)$, gives $$f(g_1(\overline x), \dots, g_n(\overline x)). $$
- *Primitive recursion.* If $h_i: \Bbb N^{n-1}\to \Bbb N$ and $g_i: \Bbb N^{n+k}\to \Bbb N$ are computable, $1\le i \le k$, then so are the functions $f_i: \Bbb N^n\to\Bbb N$, $1\le i \le k$, defined by the mutual induction as follows:
	- $f_i(0,\overline x) := h_i(\overline x)$,
	- $f_i(x+1, \overline x) := g_i(x, \overline x, f_1(x, \overline x), \dots, f_k(x, \overline x)),$
	where $\overline x = (x_1,\dots, x_n)$.
- *Unbounded minimisation.* if $g:\Bbb N^{n+1}\to \Bbb N$ is computable, then so is the function $f: \Bbb N^n \to \Bbb N$ that on input $\overline x = (x_1,\dots, x_n)$ gives the least $y$ such that $g(z, \overline x)$ is defined for all $z\le y$ and $g(y, \overline x) = 0$ if such a $y$ exists and is undefined otherwise. We denote this by $$f(\overline x) = \mu.y(g(y, \overline x) = 0).  $$
The functions defined above are called the *$\mu$-recursive functions*. The functions before the Unbounded minimisation are called the *primitive recursive functions.*

**Examples:** 
- The constant functions $\text{const}_n(\;) = n$ are primitive recursive:  $$\text{const}_n := \text s\circ \dots \circ \text s \circ \text z, $$where have $n$ compositions of $\text s$. 
- Addition is primitive recursive, since we can define $$\begin{align*}\text{add}(0, y) &:= y, \\ \text{add}(x+1, y) &:= \text s(\text{add}(x, y)).\end{align*}  $$This is an authentic definition by primitive recursion: in the rule describing recursion above, take $k = 1$, $n = 2$, $h = \pi^1_1$, and $g = \text s\circ \pi^3_3$. Then $$ \begin{align*}\text{add}(0, y) &:= h(y) = y, \\ \text{add}(x+1, y) &:= g(x, y, \text{add}(x, y)) = \text s( \text{add}(x, y).\end{align*} $$
- Multiplication is primitive recursive, since $$\begin{align*}\text{mult}(0, y) &:= 0, \\ \text{mult}(x+1, y) &:= \text{add}(y, \text{mutl}(x, y)).\end{align*} $$
- Exponentiation is primitive recursive, since  $$\begin{align*}\text{exp}(x, 0) &:= 1, \\ \text{exp}(x, y+1) &:= \text{mult}(x, \text{exp}(x, y)).\end{align*}  $$
- The predecessor function $$x\stackrel{.}- 1 :=\begin{cases}x-1, & x >0,\\ 0 & x= 0,\end{cases}  $$is primitive recursive $$\begin{align*}0\stackrel{.}-1 &:= 0, \\ (x+1) \stackrel{.}-1 &:= x.\end{align*}$$
- Proper subtraction $$x\stackrel{.}-y := \begin{cases} x-y & x \ge y, \\0 & x < y,\end{cases} $$is primitive recursive, and can be defined from the predecessor in exactly the same way that the addition is defined from successor.
- The sign function is primitive recursive $$\text{sign}(x) := 1\dot- (1\dot-x) = \begin{cases} 1 & x > 0,\\ 0 & x = 0.\end{cases} $$
- The relations $<, \le, > \ge, =$ and $\ne$ considered as $(0, 1)$-valued functions are all primitive recursive; for example $$\text{compare}_\le (x, y) := 1\dot- \text{sign}(x\dot-y).$$
- Functions can de defined by cases, since we can use multiplication by $\text{compare}_\square$, where $\square$ just represents the relation we want to use.
- Inverses of certain functions can be defined. 

**Def:** A general recursive function is called *total recursive function* if it is defined for every input. 

Observe that all primitive recursive functions are total, whereas a $\mu$-recursive function may not be. There exist total computable functions that are not primitive recursive. One example is the *[[Ackermann's function]]:* $$\begin{align*} A(0, y) &:= y+1 \\ A(x+1, 0) &:= A(x, 1) \\ A(x+1, y+1) &:= A(x, A(x+1, y))\end{align*}$$
**Th:** A general recursive function is *total* iff it can be computed by a total Turing machine.