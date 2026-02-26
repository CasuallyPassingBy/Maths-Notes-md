---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Lambda Calculus]], [[Other Formalisms Equivalent to General Computation]], [[Turing Machines]]

Combinatory logic is a form of a variable-free $\lambda$-calculus. It was first invented to study the mathematics of symbol manipulation, especially substitution. The systems consists of terms called *combinators* that are manipulated using *reduction rules*.

There are two primitive combinators $S$ and $K$, which are just symbols, as well as countable set of variables $\{X, Y, \dots\}$. More complicated combinators are formed inductively: $S, K$ and variables are combinators; and if $M$ and $N$ are combinators, then so is $MN$. Here $MN$ is just a term, a syntactic object, but we can think of $M$ as function and $N$ as its input; thus $MN$ represents the application of $M$ to $N$. As with the $\lambda$-calculus, this operation is not associative, so we use parentheses to avoid to ambiguity. By convention, a string of applications associates to the left; thus $XYZ$ should be parsed as $(XY)Z$. 

Computation proceeds according to two reduction rules, one for $S$ and one for $K$. For any terms $M, N$ and $P$,
- $SMNP \to MP(NP)$,
- $KMN \to M$.
Computation in this system consists of a sequence of reduction steps applied to subterms of a term.

Other combinators can be built from $S$ and $K$. For example, the combinator $I := SKK$ acts ad the identity function. 

Let $B = SK$. Whereas $K$ picks out the first element of a pair, $B$ picks out the second element $BXY = SKXY → KY(XY) →Y$.

One can construct fancy combinators from $S$ and $K$ that can rearrange symbols in every conceivable way. For example, to take two inputs and apply the second to the first, use the combinator $C := S(S(KS)B)K$. $$CXY  \to XY.$$
There is a theorem that says that no matter how you want to rearrange your inputs, there is a combinator built from $S$ and $K$ only that can do it. In other words, for any term $M$ built from $X_1,\dots, X_n$ and te application operator, there is a combinator $D$ built from $S$ and $K$ only such that  $$DX_1X_2\cdots X_n \xrightarrow{\,*\,} M. $$
This theorem is called *combinatorial completeness.*

There is a *paradoxical combinator* $SII (SII)$, which corresponds to the term $(\lambda x.xx)(\lambda x.xx)$. 

Like the $\lambda$-calculus, combinatory logic is powerful enough to simulate Turing machines. 