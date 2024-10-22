---
tags:
  - ComplexAnalysis
  - RingTheory
---
Subjects: [[Complex Analysis]], [[Ring Theory]]

**Def:** The set of the complex numbers, denoted as $\mathbb{C}$, is given as the set

$$ \Bbb{R}[i] = \Bbb C = \{a +bi \mid a, b \in \Bbb R\land i^2 = -1\} $$

with the following operations:

- $(a+bi)+(c+di) = (a+c)+(b+d)i$
- $(a+bi)(c+di) = (ac-bd)+(ad+bc)i$

The tuple $(\Bbb C, +, \cdot)$ refers to the field of the complex numbers.

********Def:******** Let $z=a+bi \in \Bbb C$, then we can define the *************__complex conjugate of $z$_ denoted as $\overline z$ or $z^*$, and defined as

$$ \overline z = a -bi $$

**********Def:********** Let $z = a+bi \in \Bbb C$ we can define the ******************real and imaginary part operators,****************** denoted by $\Re$ and $\Im$ respectively

$$ \Re (z) = a \quad \text{ and } \quad \Im(z) = b $$

************Prop:************ Let $z, w \in \Bbb C$, then

- $\overline{(z+w)} = \overline z + \overline w$
- $\overline{zw} = \overline z \,\overline w$
- If $w \ne 0$, then $\overline{(z/w})=\overline{z}/ \overline w$
- $\overline{(\overline z)} = z$
- $2\Re(z) = z+\overline z$
- $2 \Im(z) = z -\overline z$
- $z \overline z = a^2+ b^2$

**********Def:********** Let $z = a+bi \in \Bbb C$ we can define the ****************************_modulus or absolute value of $z$,_ denoted by $|z|$ and defined as

$$ |z| = \sqrt{a^2+b^2} $$

************Prop:************ Let $z, w \in \Bbb C$, then

- $|z| \ge 0$ and $|z| =0$ iff $z =0$
    
- $|z|^2 = z \overline z$
    
- $|z| = |\overline z|$
    
- $|\Re(z)|, |\Im(z)| \le |z| \le |\Re(z)| + |\Im(z)|$
    
- $|zw| = |z||w|$
    
- if $w \ne 0$, then $|z/w| = |z|/|w|$
    
- $|z+w| \le |z|+|w|$
    
- $z\ne 0$ then $z^{-1} = \overline z / |z|^2$
    
- Cauchy-Schwartz Inequality
    
    $$ \left|\sum_{k = 1}^n z_k w_k\right|^2 \le \left(\sum_{k = 1}^n |z_k|^2\right)\left(\sum_{k = 1}^n |w_k|^2\right) $$
    
- Lagrange’s Identity
    
    $$ \left|\sum_{k = 1}^n z_k w_k\right|^2 = \left(\sum_{k = 1}^n |z_k|^2\right)\left(\sum_{k = 1}^n |w_k|^2\right)-\sum_{k < j}|z_k\overline w_j-z_j\overline w_k|^2 $$
    

This forms a norm on $\Bbb C$, and thus a topology on $\Bbb C$.

**************Prop:************** Let $z \in \Bbb C$, there’s a $w \in \Bbb C$ such that $w^2 = z$

## Polar Representation

We can think of a complex number as $r(\cos \theta+ i\sin\theta)$, instead of $a+bi$, with $r = |a+bi|$. We can think find out that $r = |z|$, and $\theta$ is called the ***********_argument of $z$,_ denoted as $\arg z = \theta$. Similarly we know that if $\theta$ works then for any $n \in \Bbb Z$, then $\theta +2n\pi$ then we can think of the argument as $\arg z = \{\theta +2n\pi \mid n \in \Bbb Z\}$, and specifiying a specfic range of the angle is choosing a _******************branch of the argument.******************_

Then we can deduce that

$$ (r_1(\cos \theta_1+i \sin\theta_1))\cdot (r_2(\cos \theta_2+i \sin\theta_2)) = r_1r_2 (\cos (\theta_1+\theta_2)+i\sin(\theta_1+\theta_2)) $$

since $\cos \theta+i \sin\theta$ is a really commun occurance, it can be simplified as $\operatorname{cis}$ which cleans up the formula above to

$$ (r_1 \operatorname{cis}\theta_1) (r_2 \operatorname{cis}\theta_2) = (r_1r_2 \operatorname{cis}(\theta_1+\theta_2)) $$

From this we can deduce that $\arg(z_1z_2)= \arg(z_1)+\arg(z_2)$, and $\arg(\overline z) =-\arg(z)$

********Th (De Moivre’s Formula):******** If $z = r(\cos\theta + i\sin(\theta))$ and $n$ is a positive integer then

$$ z^n = r^n(\cos(n\theta)+ i \sin(n \theta)) $$

**********Cor:********** Let $w$ be a nonzero complex number with polar representation $w = r(\cos\theta+i \sin\theta)$. Then then $n$th roots of $w$ are given by the $n$ complex numbers

$$ z_k =\sqrt[n]{r} \left[\cos\left(\frac{\theta}{n}+ \frac{2\pi k}{n}\right) + \sin\left(\frac{\theta}{n}+ \frac{2\pi k}{n}\right)\right] \quad k =0, 1 \dots, n-1 $$