---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Complex Numbers]]

**Def:** The set $\Bbb C \cup \{\infty \}$ will be denoted as $\widehat{\Bbb C}$ , $\overline{\Bbb C}$, $\Bbb C^*$ or $\Bbb C_\infty$. We can also define if $z \in \Bbb C$, then ${z + \infty = \infty}$ and if $z \ne 0$, then $z \cdot \infty =\infty$ and $z/\infty =0$. Analogously, we cannot define consistently the expression such that $0\cdot \infty$, $0/\infty$, $\infty/0$, $\infty /\infty$ and even the identity ${\infty+\infty=\infty}$, but $\infty\cdot \infty= \infty$ is well defined.

This is the one-point compactification or [[Alexandroff compactification]]

We get $U \subseteq \widehat{\Bbb C}$ is open iff, $U\cap \Bbb C$ is open or if $\infty \in U$, $\Bbb C \setminus U$ is compact.    

Instead, we can think of it a **stereographic projection.** It is done considering the unit sphere centered at the origin, ${\Bbb S^2 \subseteq \Bbb R^3}$. The way the projection works is by considering the line that passes through $N = (0,0,1)$, and any point of the sphere, only intersects the $xy$ plane at a single point.

This correspondence is known as the stereographic projection of the points of the sphere ${\Bbb S^2 \setminus\{N\}}$ into the $xy$ plane. There’s no point corresponding to $N$ in the $xy$ plane.

The way we can define the steoregraphic projection we can define $E: \Bbb S^2 \to \widehat{\Bbb C}$, defined as

$$ E(x_1, x_2, x_3)= \begin{cases} \frac{x_1}{1-x_3} +i\frac{x_2}{1-x_3} & (x_1, x_2, x_3) \ne (0,0,1) \\ \infty & (x_1, x_2, x_3) = (0,0,1) \end{cases} $$

$E$ is a bijection from $\Bbb S^2$ into $\widehat{\Bbb C}$. Then we can get $E^{-1}: \widehat{\Bbb C} \to \Bbb S^2$ , defined as

$$ E^{-1}(z)= \begin{cases} \left(\frac{z+\overline z}{|z|^2+1}, \frac{z-\overline z}{i(|z|^2+1)},\frac{|z|^2-1}{|z|^2+1} \right) & z\in \Bbb C \\ \\ (0,0,1) & z= \infty \end{cases} $$

$\Bbb S^2$ is called the _Riemann Sphere._

If we have a circle on the Riemann Sphere then we know that if the circle contains $N$, then the image of the circle is a straight line. If is doesn’t contain $N$, then the image is also a circle.