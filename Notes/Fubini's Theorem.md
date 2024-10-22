---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Riemann Integral in Rn]], [[Integral over Jordan-measurable Sets]]

There can be s special notation to convey the integrating variables of a function in the case of a higher dimensional integral. Let $A$ be a Jordan-measurable set and $f:A\subseteq\Bbb R^n \to \Bbb R$. Then

$$ \int_A f = \int_A f(x_1, \dots, x_n) \, d(x_1, \dots, x_n) $$

Fubini’s Theorem in $\Bbb R^2$:

1. Let $A = [a,b]\times [c,d]$. Let $f:A\to \Bbb R$ be integrable over $A$, and the function ${f_x :[c,d] \to\Bbb R}$, defined as $f_x(y) = f(x,y)$ is integrable over for each ${x \in [a,b]}$. Then:
    
    $$ \int_A f = \int_a^b \left(\int_c^d f(x,y)\, dy\right)\, dx $$
    
    Similarly for $f_y:[a,b] \to\Bbb R$, defined as $f_y(x) = f(x,y)$ is integrable over for each ${y \in [c, d]}$. Then:
    
    $$ \int_A f = \int_c^d \left(\int_a^b f(x,y)\,dx\right)\,dy $$
    
2. Let $A = [a,b]\times [c,d]$. Let $f:R\to \Bbb R$ be continuous over $A$. Then
    
    $$ \int_A f = \int_a^b \left(\int_c^d f(x,y)\, dy\right)\, dx = \int_c^d \left(\int_a^b f(x,y)\,dx\right)\,dy $$
    

### General Fubini’s Theorem
1. Let $A \subseteq \Bbb R^n$ and $B \subseteq \Bbb R^m$ be rectangles and let $f:A \times B \subseteq \Bbb R^n \times \Bbb R^m\to \Bbb R$ be bounded. If $f$ is integrable and $f_x:B\to \Bbb R$, defined as $f_x(y) =f(x,y)$, be integrable for each $x \in A$. Then
    $$ \int_{A\times B} f= \int_A \left(\int_B f(x, y) \, dy\right)\,dx $$
    
    Similarly for $f_y:A \to\Bbb R$, defined as $f_y(x) = f(x,y)$ is integrable over for each ${y \in B}$. Then:
    $$ \int_{A\times B} f= \int_B \left(\int_A f(x, y) \, dx\right)\,dy $$
    
2. If $f:A\times B\subseteq \Bbb R^n\times \Bbb R^m \to \Bbb R$ is continuous on $A\times B$, then $$ \int_{A\times B} f (x,y)\, d(x,y)= \int_A \int_B f(x, y) \, dy\,dx = \int_B \int_A f(x, y) \, dx\,dy $$

This last part states, that we can choose the order of integration if the function is continuous, making it easier to solve the integral.

Using Fubini we can get that the Jordan measure of $B_r(\mathbf 0) \subseteq \Bbb R^n$ is equal to
$$ J(B_r(\mathbf 0)) = V_n(r) = \frac{\pi^{n/2}}{\Gamma\left(\frac{n}{2}+1\right)} R^n $$

In the case, of $r=1$, it is simlpy denoted as $V_{2n}$. Then we have the surprising connection
$$ \sum_{n = 0}^\infty V_{2n} = e^\pi $$
which is known as the Genfold’s constant


### Consequences
Some important consequences show that for regions of the form, given $\alpha,\beta:[a,b] \to \Bbb R$ continuous and $\alpha \le \beta$, ${D = \{(x,y) \in \Bbb R^2\mid a\le x \le b \land \alpha(x) \le y \le \beta(x)\}}$o is Jordan-measurable and we can integrate $f$ over $D$ as
$$ \int_D f = \int_a^b \int_{\alpha(x)}^{\beta(x)} f(x,y) \,dy\,dx $$
We can flip the dependencies of $x$ and $y$, and still integrate over $D$ we just need to be careful about it.
This concept can be extended to higher dimensions to let us integrate over different regions.