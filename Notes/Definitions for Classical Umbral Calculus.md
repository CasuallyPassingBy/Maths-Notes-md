---
tags: []
---
Subjects: [[Umbral calculus]]
Links: [[Delta Operators]], [[Dual Spaces]]

Let $P$ be the algebra of polynomials in the single variable $x$ over the field $C$ of characteristic zero. Let $P^*$ be the dual vector space of $P$. $$\langle L \mid p(x)\rangle$$borrowed notation from physics, to denote the action of the linear functional $L$ on a polynomial $p(x)$, and we recall that the vector space operations on $P^*$. 

Since a linear functional is uniquely determined by its action on on a basis, $L$ is uniquely determined by the sequence of constant $\langle L \mid x^n\rangle$ 

We denote $\mathscr F$ denote the algebra of formal power series in the variable $t$ over the field $C$. The formal power series $$f(t) = \sum_{k = 0}^\infty \frac{a_k}{k!}t^k$$defines a linear functional on $P$ by setting $$\langle f(t) \mid x^n\rangle  =a_n$$
for all $n \ge 0$. In particular $$\langle t^k \mid x^n \rangle = n! \delta_{n, k}$$
Actually, any linear functional $L$ in $P^*$ has the form $$f_L(t) = \sum_{k = 0}^\infty \frac{\langle L \mid x^k\rangle}{k!} t^k$$then we get that $$\langle f_L(t) \mid x^n\rangle = \langle L \mid x^n\rangle$$
**Th:** The map $L \mapsto f_L(t)$ is a vector space isomorphism from $P^*$ onto $\mathscr F$.

Given this isomorphism between the vector space $P^*$ and the algebra $\scr F$. Then we can identify each linear functional with a formal power series and we can define an algebra structure on $P^*$, namely the algebra of formal power series. We shall call $\scr F$ the *umbral algebra*. 

**Prop:** If $f(t), g(t) \in \scr F$, then $$\langle f(t)g(t) \mid x^n\rangle = \sum_{k = 0}^n {n \choose k} \langle f(t) \mid x^k\rangle \langle g(t) \mid x^{n-k}\rangle$$
**Prop:** If $f_1, \dots, f_, \in \scr F$, then $$\langle f_1(t) \cdots f_m(t)\mid x^n\rangle = \sum {n \choose i_1, \dots, i_m} \langle f_1(t) \mid x^{i_1}\rangle \cdots \langle f_m(t) \mid x^{i_m}\rangle$$
where $i_1 + \dots+ i_m =n$

**Def:** the *order* $o(f(t))$ of a power series $f(t)$ is the smallest integer $k$ for which the coefficient $t^k$ doesn't vanish. We take $o(f(t)) = \infty$ if $f(t) = 0$. 

We have a couple of things that are easy to see:
- $o(f(t)g(t)) = o(f(t))+o(g(t))$
- $o(f(t)+g(t)) \ge \min\{o(f(t)), o(g(t))\}$ 
- The series has a multiplicative inverse if $o(f(t)) = 0$. 

**Def:** if $o(f(t)) = 1$, then the formal power series $f(t)$ has a a compositional inverse $\bar f(t)$, satisfying $f (\bar f(t)) = \bar f(f(t)) = t$. A series for which $o(f(t)) = 1$ will be called a *delta series*. 

The sequence $f(t)^k$ of powers of a delta series form a *pseudobasis* for $\scr F$. That is, for any series $g(t)$ in $\scr F$ there exists a unique sequence of constants $a_k$ for which $$g(t) = \sum_{k = 0}^\infty a_k f(t)^k$$

**Prop:** If $o(f(t)) > \deg(p(x))$, then $\langle f(t) \mid p(x) \rangle = 0$

**Prop:** If $o(f_k(t)) = k$ for all $k \ge 0$, then $$\left\langle \left.\sum_{k = 0}^\infty a_k f_k(t)\; \right|\; p(x)\right\rangle = \sum_{k = 0}^\infty a_k \langle f_k(t) \mid p(x)\rangle$$for all $p \in P$, the second sum is finite

**Prop:** If $o(f_k(t)) = k$ for all $k \ge 0$ and if $$\langle f_k(t) \mid p(x) \rangle = \langle f_k(t) \mid q(x)\rangle$$for all $k$, then $p(x) = q(x)$. 

**Prop:** If $\deg p_k(t) = k$ for all $k \ge 0$ and if $$\langle f(t) \mid p_k(x) \rangle = \langle g(t) \mid p_k(x)\rangle $$for all $k$, then $f(t) = g(t)$

We actually have two nice things in particular $$\langle t^k \mid p(x) \rangle = p^{(k)}(0)$$for all $k$. 

**Def:** When we are considering a delta series $f(t) \in \scr F$ as a linear functional we will refer to it as *delta functional*. Similarly, when we are considering invertible series as a linear functional, we use the term *invertible functional*. 

**Prop:** The series $f(t)$ is a delta functional iff $$\langle f(t) \mid 1\rangle = 0 \qquad \langle f(t) \mid x\rangle \ne 0$$
**Prop:** The series $f(t)$ is an invertible functional iff $\langle f(t) \mid 1 \rangle \ne 0$.

**Prop:** If $f(t) \in \scr F$, then $$\langle f(t) \mid x p(x) \rangle = \langle \partial_t f(t) \mid p(x)\rangle$$ for all polynomials.  

**Prop:** For any $f(t) \in \scr F$, and $p(x) \in P$, $$\langle f(t) \mid p(ax)\rangle = \langle f(at) \mid p(x)\rangle$$
# Linear Operators

We are going to adopt a weird notation. Let $f(t)$ be a power series $$f(t) = \sum_{k = 0}^\infty \frac{a_k}{k!}t^k$$we can make it a linear operator on $P$ defined by $$f(t) x^n = \sum_{k = 0}^\infty {n \choose k} a_k x^{n-k}$$
Meaning that we use juxtaposition $f(t)p(x)$ to denote the action of the operator $f(t)$ on the polynomial $p(x)$. 

As with linear functional, we note two elements $f(t), g(t) \in \scr F$ are equals as formal power series iff they are equal as linear operators. We can also conclude that $$[f(t) g(t)]p(x) = f(t)[g(t) p(x)]$$for all $f(t), g(t) \in \scr F$ and $p(x) \in P$, and so we can write $f(t)g(t)p(x)$ without ambiguity, Using the commutativity of the product in $\scr F$, we get that $$f(t)g(t)p(x) = g(t)f(t)p(x)$$for all $f(t), g(t) \in \scr F$ and $p(x) \in P$. 

**Def:** When we think of a delta (or invertible) series as an operator, we shall refer to it as a *delta* (or *invertible*) *operator*.

**Prop:** If $o(f(t)) > \deg p(x)$, then $f(t)p(x) = 0$

**Prop:** If $o(f_k(t)) = k$ for all $k \ge 0$, then $$\left[\sum_{k = 0}^\infty a_k f_k(t)\right] p(x) = \sum_{k = 0}^\infty a_k [f_k(t)p(x)]$$for all $p(x) \in P$, the second one being a finite sum

**Prop:** If $o(f_k(t)) = k$ for all $k \ge 0$ and if $f_k(t) p(x) = f_k(t)q(x)$ for all $k$, then $p(x) = q(x)$

**Prop:** If $\deg p_k(x) = k$ for all $k\ge 0$ and if $f(t)p_k(x) = g(t)p_k(x)$ for all $k$, then $f(t) = g(t)$. 

**Prop:** If $f(t), g(t) \in \scr F$ and $p(x) \in P$, then $$\langle f(t) g(t) \mid p(x) \rangle = \langle g(t) \mid f(t) p(x)\rangle$$