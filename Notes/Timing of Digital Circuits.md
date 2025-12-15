---
tags:
  - DigitalCircuits
---
Subjects: [[Digital Circuits]]
Links: [[Combinational Building Blocks for Digital Circuits]], [[Karnaugh Maps]]

One of the most challenging issues in circuit design is *timing*: making a circuit run fast.

The output takes time to change in response to an input change. There's a *delay* between an input change and the subsequent output change for a buffer. We use a *timing diagram*; it portrays the *transient response* of the buffer circuit when an input changes. The transition form $\text{LOW}$ to $\text{HIGH}$ is called a *rising edge*. Similarly, the transition from $\text{HIGH}$ to $\text{LOW}$ is called *falling edge*. We measure delay from the $50\%$ *point* of the inpute signal, $A$, to the $50\%$ point of the output signal, $Y$. The $50\%$ is the point at which the signal is half-way between $\text{LOW}$ and $\text{HIGH}$ values as it transitions. 
![[Pasted image 20251212004720.png]]

An example of a Timing diagram, the blue arrow indicates the rising edge of $Y$ is caused by the rising edge of $A$.

![[Pasted image 20251212005526.png]]
The image above shows a buffer propagation delay and contamination delay in blue and grey respectively. The image shows that $A$ is initially either $\text{HIGH}$ or $\text{LOW}$ and changes to the other state at a particular time. In response, $Y$ changes some time later. The arcs indicate that $Y$ may start to change $t_{cd}$ after $A$ transitions and $Y$ definitely settles to its new value within $t_{pd}$. 

Calculating $t_{pd}$ and $t_{cd}$ requires delving into the lowered levels of abstractions beyond my scope (at least for now). However, manufacturers normally supply data sheets specifying these delays for each gate. 

Along with the factors already listed, propagation and contamination delays are also determined by the *path* of the signal takes from input to the output. The *critical path* is the longest, and therefore the slowest, path, because the input travels through more gates to the input. This path is critical becase it limits the sped at which the circuit operates. The *short path*, as its name implies, is the shortest, and thus fastest path through the circuit, because the input travels through the fewest gates to the input.

The propagation delay of a combinatorial circuit is the sum of the propagation delays through each element on the critical path. The contamination delay is the sum of the contamination delays through each element of the short path. 

## Glitches

We have only discussed the case where a single input transition causes a single output transition. However, it is possible that a single input transition can cause *multiple* output transitions. These are called *glitches* or *hazards*. Although glitches usually don't cause problems, 

In general, a glitch can occur when a sinlge variable crosses the boundary between two prime implicants in a $K$-map. We can eliminate the glitch by adding redundatn to the $K$-map to cover these boundaries. This of course comes at a cost of extra hardware.

However, simultaneous transitions on multiple inputs can also cause glitches. These glitches cannot be fixed by adding hardware. Because the vat majority of interesting systems have simultaneous (or nearly simultaneous) transitions on multiple inputs, glitches are a fact of life in most circuits. Just being aware of there existence is already important. 