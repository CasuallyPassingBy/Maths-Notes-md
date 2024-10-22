---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[First Order Differential Equations]]
********Def:******** A ********first order separable differential equation******** is of the form

$$ \frac{dy}{dx} = F(x, y) = f(x) g(y) $$

Similarly using differentials we can get the following

$$ M(x)\, dx + N(x)\, dy =0 $$

### Method

From the first form we can get that

$$ \frac{1}{g(y)}\frac{dy}{dx} = f(x) $$

If we antidifferentiate with respect to $x$, we get that

$$ G(y) =\int \frac{dy}{g(y)} = \int f(x) \, dx $$

From this we can solve for $y$ by

$$ y = G^{-1}\left(\int f(x)\, dx\right) $$