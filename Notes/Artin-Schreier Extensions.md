---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Finite Fields]], [[Splitting Fields and Normal Field Extensions]], [[Characteristic of a Ring]], [[Galois Field Extensions]], [[Solvable Polynomials and Radical Extensions]]

Let $K$ be a field of characteristic $p > 0$, and $E/K$ a cyclic extension of order $p^{m-1}$ with $m > 1$. 

**Def:** An Artin-Schreier polynomial $A_\alpha(x) \in K[x]$ is of the form $$x^p-x-\alpha,$$with $\alpha \in K$. 

**Obs:** An almost immediate property of Artin-Schreier polynomials that we can notice is the equation $$A_\alpha(x+y) = A_\alpha(x)+ A_\alpha(y)- A_\alpha(0) $$

**Prop:** If $A_\alpha(x)$ has a root in $K$, then all roots of $A_\alpha(x)$ is in $K$. Otherwise, $A_\alpha(x)$ is irreducible over $K$. In this case, let $\theta$ be a root of $A_\alpha(x)$, then $K(\theta)/K$ is a cyclic extension of degree $p$. We see that $K(\theta)$ is the splitting field of $A_\alpha(x)$, the generator of $\text{Gal}(K(\theta)/K)$ is $\sigma(x) = x+1$. 

**Def:** The field extension $E/K$ is called an Artin-Schreier extension if $E= K(\theta)$ for some $\alpha \in L$.  

**Cor:** If $A_\alpha(x)$ is an Artin-Schreier polynomial in $\Bbb F_p$, and $\alpha \in \Bbb F_p^\times$, then $\Bbb F_p(\theta) \cong \Bbb F_{p^p}$. 

Let's consider the case where $L/K$ is a cyclic extension of degree $n$ such that $\text{char }K \mid n$. 

**Prop:** Let $L/K$ be a cyclic extension of degree $n$, where $n = p^k m$, $\text{char K} = p> 0$, and $p \not\mid m$, then there exists a sequence of extensions $$K \subseteq M_k \subseteq\cdots\subseteq M_0 \subseteq L $$such that $L/M_0$ is a cyclic extension of degree $m$, and foro $i \in \{1,\dots, k\}$ $M_i/M_{i+1}$ is a cyclic extension of degree $p$. 

With this proposition we only need to consider the case where $n = p = \text{char K} = p$. 

**Artin-Schreier Theorem:** Let $K$ be a field of characteristic $p \ne 0$.
- If $L/K$ is cyclic extension of degree $p$, then $L$ is the splitting field of a an irreducible polynomial $x^p-x-a\in K[x]$. In fact, $L = K(\alpha)$ where $\alpha$ is any root of $x^p-x-a$. 
- Reciprocally, if $L$ is the splitting field of the polynomial $x^p-x-a\in K[x]$, then $L/K$ is cycic. Furthermore,
	- The polynomial $x^p-x-a$ has all of its roots in $K$, so $L = K$, or
	- The polynomial $x^p-x-a$ is irreducible over $K$, and thus $L/K$ is cyclic of degree $p$, and $L = K(\alpha)$, with $\alpha$ is any root of $x^p-x-a$. 