---
tags:
  - ComputationTheory
  - Logic
---
Subjects: [[Theory of Computation]], [[Logic]]
Links: [[Arithmetic of Natural Numbers]], [[Turing Machines]], [[Computation Reducibility]], [[Decidable and Undecidable Problems]], [[Oracle Machines and Relative Computation]], [[Natural Numbers]], [[ZF Axioms]]

The first-order language of number theory $L$ is a forma language for expressing properties of the natural numbers $\Bbb N$. The language is built from the following symbols:
- variables $x, y, z, \dots$ ranging over $\Bbb N$;
- operator symbols $+$ and $\cdot$;
- constant symbols $0$, and $1$;
- relation symbol $=$;
- quantifiers $\forall$ and $\exists$;
- propositonal operators $\lor$, $\land$, $¬$, $\to$ and $\leftrightarrow$;
- parentheses. 

We can define other comparison relations beside $=$;
- $x \le y := \exists z \; x+z =y$,
- $x < y := \exists z \; x +z = y \land ¬(z = 0)$. 

If there are no free variables, then the formula is called a *sentence*. Every sentence has an well-defined truth value under its natural interpretation in $\Bbb N$. 

Many useful number-theoretic concepts can be formalised in this language.
- '$q$ is the quotient and $t$ the remainder obtained when dividing $x$ by $y$ using integer division' $$\text{INTDIV}(x, y, q, r) := x = qy+r \land 0 \le r \land r <y.$$
- '$y$ divides $x$' $$\text{DIV}(y,x) := \exists q \; \text{INTDIV}(x, y, q, 0). $$
- '$x$ is even' $$\text{EVEN}(x):= \text{DIV}(2, x). $$
- '$x$ is odd' $$\text{ODD}(x) := ¬\text{EVEN}(x).  $$
- '$x$ is prime'  $$\text{PRIME}(x) := 2 \le x \land  \forall y(\text{DIV}(y, x) \to (y= 1 \lor y =x)) $$
- '$x$ is a power of two'  $$\text{POWER}_2(x) := \forall y (\text{DIV}(y, x) \land \text{PRIME}(y)\to y = 2). $$
- '$y$ is a power of two, say $2^k$, and the $k$th bit of the binary representation of $x$ is $1$' $$\text{BIT}(x, y) = \text{POWER}_2(y) \land \forall q\forall r (\text{INTDIV}(x,y, q, r)\to \text{ODD}(q)). $$

The set of true sentences in this language is called *first-order number theory* and is denoted $\text{Th}(\Bbb N)$. The *decision problem* for number theory is to decide whether a given sentence is true; that is, whether a given sentence is in $\text{Th}(\Bbb N)$. 

# Peano Arithmetic

Among the axioms of Peano arithmetic, there are axioms that apply to first-order logic in general and not particular to number theory, such as axioms for manipulating
- propositional formulas, such as $(\varphi\land \psi) \to \varphi$;
- quantifiers, such as $(\forall x\varphi(x)) \to \varphi(n)$ for some $n$; and
- equality, such as $\forall x\forall y \forall z(x = y \land y =z \to x =z)$. 

Peano Arithmetic has the following axioms particular to number theory
- $\forall x \; ¬(0 = x +1)$
- $\forall x\forall y (x+1 = y+1 \to x = y)$
- $\forall x\;  x + 0 = x$
- $\forall x \forall y  \; x + y+1 = (x+y)+1$
- $\forall x\; x\cdot 0 = 0$
- $\forall x \forall y \; x \cdot (y+1) = (x\cdot y ) +x$
- $(\varphi(0)\land \forall x (\varphi(x) \to \varphi(x+1)))\to \forall x \; \varphi(x)$ where $\varphi(x)$ denotes any formula with one free variable $x$. 
The last axiom is called the *induction axiom*. It is actually an axiom *scheme* because it represents infinitely many axioms, one for each $\varphi(x)$. 

There are also two *rules of inference* for deriving new theorems form old: $$\frac{\varphi \quad \varphi \to \psi}{\psi}, \qquad \frac{\varphi}{\forall x\; \varphi}.$$These two rules are called *modus ponens* and *generalisations*, respectively. 

A *proof* of $\varphi_n$ is a sequence $\varphi_0, \varphi_1,\dots, \varphi_n$ of formulas such that each $\varphi_i$ either is an axiom or follows from formulas earlier in the list by a rule of inference. A sentence of the language is a *theorem* of the system if it has a proof. 

A proof system is said to be *sound* if all theorems are true; that is, if it is not possible to prove a false sentence. 

A proof system is said to be *complete* if all true statements are theorems of the system; that is, if the set of theorems coincides with $\text{Th}(\Bbb N)$. 

# Turing's Proof

Let us consider a modified version the Peano axioms where we exclude the product. We can denote this model by $(\Bbb N,  +)$. 

**Th:** The set $\text{Th}(\Bbb N, +)$ is decidable.

The set of theorems of Peano Arithmetic is certainly recursively enumerable. We can enumerate the theorems by enumerating all the axioms and systematically applying the rules of inference in all possible ways, emitting every sentence that is ever derived. 

**Th:** $\text{Th}(\Bbb N)$ is not recursively enumerable.

We prove this by a reduction $\overline{\mathsf{HP}} \le_\text m \text{Th}(\Bbb N)$. So given $M\#x$, we show how to produce a sentence $\gamma$ in the language of number theory such that  $$M \#x \in \overline{\sf HP}\iff \gamma \in \text{Th}(\Bbb N); $$that is, $M$ doesn't halt on $x$ iff $\gamma$ is true. 

In other words, given $M$ and $x$, we want to construct a sentence $\gamma$ in the language of number theory that says '$M$ doesn't halt on $x$'. This will be possible because the language of number theory is strong enough to talk about Turing machines and whether or not they halt. 

Assume that configurations of $M$ are encoded over a finite alphabet $\Delta$ of size $p$, where $p$ is prime. We use the $p$-ary representation for convenience. 

Let the symbols of the start configuration of $M$ on $x = a_1\cdots a_n$ be encoded by the $p$-ary digits $k_0,\dots, k_n$  

| $\vdash$ | $a_1$ | $a_2$ | $a_3$ | $\cdots$ | $a_n$ |
| -------- | ----- | ----- | ----- | -------- | ----- |
| $s$      | $─$   | $─$   | $─$   | $\cdots$ | $─$   |
| $k_0$    | $k_1$ | $k_2$ | $k_3$ | $\cdots$ | $k_n$ |

Let the blank symbol $\textvisiblespace$ be encoded by the $p$-ary digit $k$. 

Let $C$ be the set of all sextuple $(a,b,c,d,e,f)$ of $p$-ary digits that if the three elements of $\Delta$ represented by $a, b,c$ occur consecutively in configuration $\alpha_i$, and if $d, e$ and $f$ occur in the corresponding locations in $\alpha_{i+1}$, then this would be consisten with the transition function $\delta$. 

Now we define some formulas
- 'The number $y$ is a power of $p$: '$$\text{POWER}_p(y) := \forall z(\text{DIV}(z, y) \land \text{PRIME}(z) \to z = p)  $$
- 'The number $d$ is a power of $p$ and specifies the length of $v$ as a string over $\Delta$' $$\text{LENGHT}(v, d) := \text{POWER}_p(d) \land v < d.$$
- 'The $p$-ary digit of $v$ is at position $y$ in $b$' $$\text{DIGIT}(v, y, b ) := \text{POWER}_p(y) \land \exists u \exists a (v = a+by+upy \land a <y  \land b <p) $$
- 'The three $p$-ary digits of $v$ at position $y$ are $b,c$ and $d$' $$\begin{align*}
  \text{3DIGIT}(v, y, b,c, d) &:= \text{POWER}_p(y) \land \exists u \exists a \\&(v = a+by+cpy+dppy+upppy \land a <y  \land b <p\land c < p \land d <p)\end{align*}$$
- 'The three $p$-ary digits of $v$ at position $y$ match the three $p$-ary digits of $v$ at $z$ according to $\delta$'$$\begin{align*}
  \text{MATCH}(v, y,z) &:= \text{POWER}_p(y) \land \text{POWER}_p(z) \land \\&\bigvee_{(a,b,c, d, e, f)\in C}\text{3DIGIT}(v,y,a,b, c) \land \text{3DIGIT}(v, z,d, e, f)\end{align*} $$
- 'The string $v$ represents a string of succesive configuration of $M$ of length $c$ up to $d$' = 'All pairs of three digit sequences exactly $c$ apart in $v$ match according to $\delta$' $$\begin{align*}\text{MOVE}(v, c, d) :=& \text{POWER}_p(c)\land \text{POWER}_p(d) \land\;  \\& \forall y(\text{POWER}_p(y) \land yppc <d) \to \text{MATCH}(v, y, yc) \end{align*}$$
- 'The string $v$ starts with the start configuation of $M$ on input $x = a_1\cdots a_n$ added with blanks out to length $c$' $$\begin{align*}
  \text{START}(v, c) := &\text{POWER}_p(c) \land \bigwedge_{i = 0}^b \text{DIGIT}(v, p^i, k_i) \land p^n < c  \\& \; \land \; \forall y(\text{POWER}_p(y) \land p^n < y <c \to \text{DIGIT}(v, y, k)) \end{align*} $$
- 'The string $v$ has a halt state in it somewhere' $$\text{HALT}(v, d) := \exists y \left(\text{POWER}_p(y) \land y<d\land \bigvee_{a\in H} \text{DIGIT}(v, y, a)\right) $$Here $H$ is the set of all $p$-ary digits corresponding to symbols of $\Delta$ containing halt states.
- 'The string $v$ is a valid computation history of $M$ on $x$' $$\begin{align*}\text{VALCOMP}_{M, x}(v) := &\; \exists c\exists d (\text{POWER}_p(c) \land c<d\land\text{LENGTH}(v, d)\\& \text{START}(v, c) \land \text{MOVE}(v, c, d) \land \text{HALT}(v, d) )\end{align*} $$
- 'The machine $M$ does not halt on $x$' $$¬\exists v \text{VALCOMP}_{M, x}(v). $$
This concludes the proof of the incompleteness.

This means that $\text{Th}(\Bbb N)$ must contain properly the set of theorems of Peano arithmetic, so there must be true statements that cannot be proved.

# Gödel's Proofs

We use the symbols $\vdash$ and $\models$ for provability in Peano arithmetic and truth, respectively. That is.
- $\models \varphi$, is defined to be, sentence $\varphi$ is true in $\Bbb N$,
- $\vdash \varphi$, is defined to be, sentence $\varphi$ is provable in Peano arithmetic.

To say that Peano arithmetic is *sound* says that every theorem of Peano arithmetic is true; in other words, for any sentence $\varphi$, if $\vdash \varphi$, then $\models \varphi$. The soundness of Peano arithmetic can be proved by induction on the length of proofs, using the fact that all the axioms of Peano arithmetic are true and the induction rules preserve 'truth'. 

Let formulas of number theory be coded as natural numbers in some reasonable way. Fix this coding and let $\ulcorner \varphi\urcorner$ denote the code of the formula $\varphi$. 

**Gödel's Fixpoint Lemma:** For any formula $\psi(x)$ with one free variable $x$, there exists a sentence $\tau$ such that  $$ \vdash \quad \tau \leftrightarrow \psi(\ulcorner \tau\urcorner);$$that is, the sentences $\tau$ and $\psi(\ulcorner \tau\urcorner)$ are provably equivalent in Peano arithmetic. 

Now we see that the language of number theory is also strong enough to talk about provability in Peano arithmetic. In particular, it is possible to code sequences of formulas as numbers and write down a formula $\text{PROOF}(x, y)$ that asserts that the sequence of formulas whose code is given by $x$ is legal proof in Peano arithmetic and constitues a proof of the formula whose code is given by $y$. That is, for any sequence $\pi$ of formulas and formula $\varphi$,  $$\vdash \text{PROOF}(\ulcorner\pi\urcorner,\ulcorner\varphi\urcorner )\iff \text{$\pi$ is a proof in PA of }\varphi.  $$Provability in Peano arithmetic is then encoded by the formula $$\text{PROVABLE}(y) := \exists x \text{PROOF}(x, y). $$Then for any sentence $\varphi$ of $L$ $$\vdash \varphi  \iff \models \text{PROVABLE}(\ulcorner\varphi\urcorner).$$Moreover,$$\vdash \varphi \iff \vdash \text{PROVABLE}(\ulcorner\varphi\urcorner).$$
Applying the fixpoint lemma to the predicate $¬\text{PROVABLE}(x)$, we obtain a sentence $\rho$ that asserts its own unprovability $$\vdash \rho \leftrightarrow ¬\text{PROVABLE}(\ulcorner\rho\urcorner); $$in other words, $\rho$ is true iff it is not provable in Peano arithmetic. By soundness of Peano arithmetic, we have $$\models \rho \leftrightarrow ¬\text{PROVABLE}(\ulcorner\rho\urcorner). $$Then the sentence $\rho$ must be true, since if not, then $$\begin{align*}\models ¬\rho &\implies \models \text{PROVABLE}(\ulcorner\rho\urcorner) \\ &\implies \vdash \rho \\ &\implies \models \rho\end{align*}$$a contradiction. Therefore $\models \rho$. But again, $$\begin{align*}\models \rho &\implies \models ¬\text{PROVABLE}(\ulcorner\rho\urcorner) \\ &\implies \not\vdash \rho \\ &\implies \not\models \rho\end{align*}$$Thus $\rho$ is true but not provable. 

## The Second Incompleteness Theorem

Observe that there is logic going on at two levels here. The object of out study os a logical system, namely the language of number theory $L$ and its deductive system Peano arithmetic; but we are reasoning about it using another logical system, which we will call the *metasystem*. The symbols $\vdash$, $\models$, $\implies$ and $\iff$ that we used in the previous section are not symbols of $L$, but *metasymbols*, or symbols of the metasystem. The statements we made about truth and provability of sentences of $L$ are *metastatements*.

Certain metastatements about $L$ and Peano arithmetic can be encoded in $L$ using the coding scheme $\ulcorner \varphi\urcorner$ and reasoned about in Peano arithmetic. The metastatement $$\vdash \varphi  \iff \models \text{PROVABLE}(\ulcorner\varphi\urcorner)$$expresses the correctness of this encoding.

The metastatement '$\varphi$ is true' cannot be expressed in $L$. If  there was a formula $\text{TRUE}(x)$ of L$ such that for all sentences of $L$, $$\models \varphi \iff \text{TRUE}(\ulcorner\varphi\urcorner).  $$But it follows from the fixpoint lemma that no such formula can exists. If it did, then there would exist a sentence $\sigma$ such that  $$\models\sigma \iff ¬\text{TRUE}(\ulcorner\sigma\urcorner); $$but $$\models \sigma \iff \text{TRUE}(\ulcorner\sigma\urcorner),  $$which is a contradiction.

The language $L$ is not powerful enough to express the *truth* of sentences of $L$ or the *soundness* of Peano arithmetic. These are external concepts, and we must deal with them in the metasystem. However, $L$ and Peano arithmetic are powerful enough to express and reason about *provability* and *consistency*, which are internal analogues of truth and soundness, respectively. *Consitency* just means that no contradictions can be derived; in other words, $\bot$ (falsity) is not a theorem. The consistency of Peano arithmetic is expressed in $L$ as follows: $$\text{CONSIS} := ¬\text{PROVABLE}(\ulcorner \bot\urcorner).$$
Meta-arguments involving only the concepts of provability and consitency can typically be mapped down into Peano arithmetic. 

**Gödel's Second Incompleteness Theorem:** No suficiently powerful deductive system can prove its own consistency, unless it is inconsistent.

We prove the second incompleteness theorem for Peano arithmetic. But it actually holds for any sufficiently powerful deductive system, where 'sufficiently powerful' just means strong enough to encode and reason about certain metastatements involing provability and consistency such as those discussed above.

**Cor:** $\sf ZF$ set theory cannot be proven to be consisten, unless it is inconsistent.