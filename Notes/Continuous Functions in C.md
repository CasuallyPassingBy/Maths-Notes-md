---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Topological Characterization of Continuity in Rn]], [[Important Functions in Complex Numbers]]

********Def:******** Let $f: A\subseteq \Bbb C \to \Bbb C$, with $z_0 \in \operatorname{int}(A)$, then we define we say that $f$ ****_has limit $L$ as ${z \to z_0}$_ and write

$$ \lim_{z\to z_0} f(z) = L $$

when

$$ \forall \varepsilon>0\exists \delta>0\forall z \in A[0<|z-z_0| <\delta \implies |f(z)-f(z_0)|<\varepsilon] $$

All the properties of limits of functions from $\Bbb R^2$ to $\Bbb R^2$ are preserved

********Def:******** Let $f: A\subseteq \Bbb C \to \Bbb C$, and $z_0\in A$, we say that $f$ is continuous at $z_0$ if

$$ \forall \varepsilon>0\exists \delta>0\forall z \in A[|z-z_0| <\delta \implies |f(z)-f(z_0)|<\varepsilon] $$

and all of the properties of continuous functions are similar to functions from $\Bbb R^2$ to $\Bbb R^2$

************Prop:************ For every $y_0 \in \Bbb R$ the branch of the logarithm $\ln_{y_0}$ is continuous in the set

$$ \Bbb C \setminus\{r(\cos(y_0)+i\sin(y_0)) \mid r\ge 0\} $$

****************Cor:**************** The branch of the $n$th root of $z$ that has image on $A_{\alpha, n}$ is continuous on the set

$$ \Bbb C\setminus \{r(\cos(n\alpha)+i\sin(n\alpha)) \mid r\ge 0\} $$

**********Def:********** Let $f:\Omega \subseteq \Bbb C \to \Bbb C$ y $U \subseteq \Omega$

- We say that $g:U\subseteq \Bbb C \to \Bbb C$ is a branch of the $n$th root of $f$ on $U$ if
    
    $$ (g(z))^n = f(z) $$
    
    for all $z \in U$
    
- We say that $g:U\subseteq \Bbb C \to \Bbb C$ is a branch of the logarithm of $f$ on $U$, if
    
    $$ \exp(g(z)) =f(z) $$
    
    for all $z \in U$
    

************Prop:************ Let $f:\Omega \subseteq \Bbb C \to \Bbb C$ continuous on $\Omega$ and $U\subseteq \Omega$

- If $\alpha \in \Bbb R$ and $f$ are functions such that
    
    $$ f[U] \subseteq \Bbb C \setminus \{r(\cos(n\alpha)+i\sin(n\alpha)) \mid r \ge 0\} $$
    
    then the function $g:U\subseteq \Bbb C \to \Bbb C$ is defined as
    
    $$ g(z) = \left(\exp \circ \left(\frac{1}{n}\ln_{n \alpha} \circ f\right)\right)(z) $$
    
    is a continuous branch of the $n$th root of $f$ with image on $A_{\alpha,n }$. If $\alpha = -\pi/n$, we say that $g$ is the principal branch of $f$ (defined on $U$), denoted as $\sqrt[n] f$
    
- If $y_0 \in \Bbb R$, and $f$ is such that
    
    $$ f[U] \subseteq \Bbb C \setminus \{r(\cos(y_0)+i\sin(y_04)) \mid r \ge 0\} $$
    
    then the function $g:U \subseteq \Bbb C \to \Bbb C$ defined as
    
    $$ g(z) := (\ln_{y_0} \circ f)(z) $$
    
    is a continuous branch of the logarithm with image on $L_{y_0}$. If $y_0 = -\pi$, we say that $g$ is the principal branch of the logarithm of $f$ (defined on $U$) and denoted as $\ln(f)$.