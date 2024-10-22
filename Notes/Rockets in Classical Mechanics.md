---
tags:
  - ClassicalMechanics
---
Subjects: [[Classical Mechanics]]
Links: [[Linear Momentum in Classical Mechanics]]

We can use the fact that with no external forces, momentum is conserved, then

$$ \dot {\bf P} = 0 $$

then in the case of a rocket we have that mass is also variable, then the expression of momentum is

$$ m \dot{\bf v} + \dot m {\bf v} =0 $$

if we assume that a rocket is on its side, and that the mass is propelled with speed $v_\text{ex}$ (a constant), then we have that

$$ m\dot v + \dot m v_\text{ex} = 0 $$

then

$$ m\dot v = - \dot m v_\text{ex} $$
We can see that the equation above, looks a lot like $m \dot v = F$, with $-\dot m v_\text{ex}$ playing the role of the force. For this reason this product is often called **thrust**:
$$
\text{thrust} = -\dot m v_\text{ex}
$$
We can solve this getting the fact that

$$ v - v_0 = v_\text{ex}\ln\left(\frac{m_0}{m}\right) $$

In general if 
$$ \dot {\bf P} = \bf{F}^\text{ext} $$
we then get the general motion of a rocket
$$
m \mathbf{\dot v} + \dot m \mathbf{v}_\text{ex} = \mathbf F^\text{ext}
$$

If we make the added assumption that everything is working in the same axis that means that we can just consider 1 dimensional motion. 
$$
m \dot v + \dot m v_\text{ex} = F^\text{ext}
$$
with this added term, we actually get
$$
v = v_0+ v_\text{ex} \ln\left(\frac{m_0}{m}\right)+ \int_0^t \frac{F^\text{ext}}{m}\, dt'
$$
in the usual case of gravity with $F^\text{ext} = -mg$, and $v_0 =0$, then
$$
v = v_\text{ex}\ln\left(\frac{m_0}{m}\right) -gt
$$
if we add that we start from the ground we get that
$$
y = v_\text{ex}t-\frac{1}{2}gt^2-\frac{mv_\text{ex}}{k}\ln\left(\frac{m_0}{m}\right)
$$with $m = m_0 - kt$, and $\dot m = -k$. 