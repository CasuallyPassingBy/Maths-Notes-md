---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Finite Fields]], [[Splitting Fields and Normal Field Extensions]], [[Characteristic of a Ring]], [[Galois Field Extensions]]

Let $K$ be a field of characteristic $p > 0$, and $E/K$ a cyclic extension of order $p^{m-1}$ with $m > 1$. 

**Def:** An Artin-Schreier polynomial $A_\alpha(x) \in K[x]$ is of the form $$x^p-x-\alpha,$$with $\alpha \in K$. 

**Obs:** An almost immediate property of Artin-Schreier polynomials that we can notice is the equation $$A_\alpha(x+y) = A_\alpha(x)+ A_\alpha(y)- A_\alpha(0) $$

**Prop:** If $A_\alpha(x)$ has a root in $K$, then all roots of $A_\alpha(x)$ is in $K$. Otherwise, $A_\alpha(x)$ is irreducible over $K$. In this case, let $\theta$ be a root of $A_\alpha(x)$, then $K(\theta)/K$ is a cyclic extension of degree $p$. We see that $K(\theta)$ is the splitting field of $A_\alpha(x)$, the generator of $\text{Gal}(K(\theta)/K)$ is $\sigma(x) = x+1$. 

**Def:** The field extension $E/K$ is called an Artin-Schreier extension if $E= K(\theta)$ fror some $\alpha \in L 

**Cor:** If $A_\alpha(x)$ is an Artin-Schreier polynomial in $\Bbb F_p$, and $\alpha \in \Bbb F_p^\times$, then $\Bbb F_p(\theta) \cong \Bbb F_{p^p}$. 