---
tags:
  - ClassicalMechanics
---
Subjects: [[Classical Mechanics]]
Links: [[Trayectories in Physics]], [[Newton's Laws]]

We consider the resisitive force, or **drag**, $\bf f$ of the air, medium, through which an object is moving. The most obvious fact about “air resistance” is that it dependes on the speed $v$, of the object (everything will be approximated as a sphere). In addition, for in most cases the force due to motion through the air is opposite to the velocity $\bf v$.

$$ {\bf f} = -f(v) \hat{\bf v} $$

where $\hat{\bf v} = {\bf v}/|{\bf v}|$ denotes the unit vector of velocity, and $f(v)\ge 0$ is the magnitud of $\bf f$.

the function $f(v)$ that gives the magnitud of the air resistance is really complicated specially when ${\bf v}$, approaches the speed of sound. However, for lower speeds is often a good approximation to write

$$ f(v) = bv+cv^2 +O(v^3) = f_{\text{lin}} + f_{\text{quad}} + O(v^3) $$

This constants refer are measured experimentally, and are dependent on the radius of the sphere we are approximating,

$$ b = \beta D \qquad c = \gamma D^2 $$

where $D$ represents the diameter of the sphere, and the coefficients $\beta$ and $\gamma$ depend on the nature of the medium.

From Stoke’s law, the viscous drag on a sphere is

$$ f_{\operatorname{lin}} = 3 \pi \eta D v $$

where $\eta$ is the _viscosity_ of the medium, $D$ the diameter of the sphere, and $v$ is speed. Then

$$ \beta = 3\pi \eta $$

We know that the viscosity of air in STP, $\eta_{\text{air}} = 1.7 \times 10^{-5} \,\text{N}\cdot \text{s}/\text{m}^2$ . From this we can calculate ${\beta_\text{air} = 1.602\times 10^{-4}\, \text{N}\cdot \text{s}/\text{m}^2}$.

Simlarly, we can make some simplifying assumptions and get that the quadratic drag force $f_{\text{quad}}$. The rate at what the object, encounters fuild in (mass/time) is $\rho Av$, where $\rho$ is density of the fluid, $A$ is the cross sectional area of the projectile and $v$ is the speed. From this we get that

$$ f_{\text{quad}} = \kappa \rho Av^2 $$

where the proportionality constant $0\le \kappa <1$ is derived from the shape of the projectile. We get that $\kappa = 1/4$ for a sphere. For a sphere we can calculate

$$ \gamma = \frac{\pi}{16} \rho $$

Given the density of air in STP, $\rho_{\text{air}}= 1.29 \, \text{kg}/\text{m}^3$, we get that $\gamma_{\text{air}} = 0.253 \, \text{N}\cdot \text{s}^2/\text{m}^4$.

We compare the sized of the two terms, to see which one we care about.

$$ \frac{f_{\text{quad}}}{f_{\text{lin}}} = \frac{cv^2}{bv} = \frac{\gamma}{\beta}Dv = \left(\frac{\rho}{48\eta}\right)Dv $$

The constant $\rho/48 \eta$, will be reasonably important to tell us which drag force is the mos important, in the case of air in STP, we have that $\rho_{\text{air}} / 48\eta_\text{air} = 1.6\times 10^3\, \text{s}/\text{m}^2$. We have three cases of the quotient.

If $\dfrac{f_\text{quad}}{f_\text{lin}} \ll 1$

Then we neglect $f_\text{quad}$, this case is the [[Linear Air Resistance|linear drag]]

If $\dfrac{f_\text{quad}}{f_\text{lin}} \approx 1$

Then don’t neglect either, this case is the mixed drag

If $\dfrac{f_\text{quad}}{f_\text{lin}} \gg 1$

Then we neglect $f_\text{quad}$, this case is the [[Quadratic Air Resistance|quadratic drag]]