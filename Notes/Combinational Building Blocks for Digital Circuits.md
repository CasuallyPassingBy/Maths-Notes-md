---
tags:
  - DigitalCircuits
---
Subjects: [[Digital Circuits]]
Links: [[Logic Gates]], [[Boolean Equations for Digital Circuits]], [[Combinational Building Blocks for Digital Circuits]]

Combinational logic is often group into larger building blocks to build more complex systems.

# Multiplexers
*Multiplexers* are among the most commonly used combinational circuits. They choose an output from among several possible inputs based on the value of a *select* signal. A multiplexer is sometimes affectionately called a *mux*. 

The $2:1$ multipleer chooses between two data inputes based on the setect: if $S = 0$, then $Y = D_0$, and if $S = 1$, then $Y = D_1$, $S$ is also called a *control signal* because it controls what the multiplexer does.

A $2:1$ multiplexer can be built from sum-of-products logic. The boolean equation for the multiplexer may be derived with a Karnaugh map of read off by inspection.  $$Y = D_0\overline S+ D_1 \overline S.$$
## Wider Multiplexers
A $4:1$ multiplexer has four data inputs and one output. Two select signals are needed to choose among the four data inputs. The $4:1$ multiplexer can be built using sum-of-product logic, tristate buffers, or multiple $2:1$ multiplexers.

In general, a $2^N: 1$ multiplexer needs $N$ select lines. Again, the best implementation choice depends on the target technology.

Multiplexers can be used as *lookup tables* to perform logic functions. A $4:1$ multiplexer used to implement a two-input $\text{AND}$. The inputs, $A$ and $B$, serve as select lines. The multiplexer data inputs are connected to $0$ or $1$ according to the row of the truth table. In general, a $2^N$-input multiplexer can be programmed to perform any $N$-input logic function by applying $0$'s and $1$'s to the appropriate data inputs. 

With a little cleverness, we can cut the multiplexer size in halt, using only a $2^{N-1}$-input multiplexer to perform an $N$-input logic function. The strategy is to provide one of the literals, as well a $0$'s and $1$'s to the multiplexer data inputs.

## Decoders
A decoder has $N$ inputs and $2^N$ outputs. It asserts exactly one of its outputs depending on the input combination. The outputs are called *one-hot*, because exactly one is 'hot' $(\text{HIGH})$ at a given time.

A simple truth table of a $2: 4$ decoder is 

| $A_1$ | $A_0$ | $Y_3$ | $Y_2$ | $Y_1$ | $Y_0$ |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 0     | 0     | 0     | 0     | 0     | 1     |
| 0     | 1     | 0     | 0     | 1     | 0     |
| 1     | 0     | 0     | 1     | 0     | 0     |
| 1     | 1     | 1     | 0     | 0     | 0     |
And they are fairly simple to do only using $\text{NOT}$ and $\text{AND}$ gates.

Decoders can be combined with $\text{OR}$ gates to build logic functions. When using decoders to build logic, it is easiest to express functions as a truth table or in canonical sum-of-product form. An $N$ input function with $M$ $1$'s in the truth tbale cab be built with an $N: 2^N$ decoder and an $M$-input $\text{OR}$ gate attached to al the minterms containing $1$'s in the truth table. This concept will be applied to the building of Read Only Memories (ROMs). 

