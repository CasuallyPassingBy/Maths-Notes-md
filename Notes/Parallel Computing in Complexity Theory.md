---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]], [[Boolean Circuit Complexity]], [[The Complexity Classes L and NL]], [[The Complexity Class P]]

A *parallel computer* is one that can perform multiple operations simultaneously. Parallel computers may solve certain problems much faster than *sequential computers*, which can only do a single operation at a time. In practice, the distinction between the two is slightly blurred because most real computers are designed to use some parallelism as they execute individual instructions. We focus here on *massive* parallelism whereby a huge number of processing elements are actively participating in a single computation.

# Uniform Boolean Circuits

One of the most popular models in theoretical work on parallel algorithms is called *Parallel Random Access Machine* or *PRAM*. In the PRAM model, idealised processors with a simple instruction set patterned on actual computers interact with shared memory. 

Boolean circuits have certain advantages and disadvantages as a parallel computation model. On the positive side, the model is simple to describe, which make proof easier. Circuits also bear an obvious resemblance to actual hardware designs and in the sense the model is realistic. On the negative side, circuits are awkward to 'program' because the individual processors are so weak. 

In the Boolean circuit model of a parallel computer, we take each gate to be an individual processors, so we define the *processor complexity* of a Boolean circuit to be the size. We consider each processor to compute its function in a single time step, so we define *parallel time complexity* of a Boolean circuit to be its depth, or the longest distance from an input variables to the output gate. 

