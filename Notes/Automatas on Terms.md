---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Finite Automaton]], [[Strings and Languages]], [[Operations and Structures]], [[Myhill-Nerode Theorem]]

**Def:** A *signature* is an alphabet $\Sigma$ consisting of various *function* and *relation symbols* in which each symbol is assigned a natural number, called it *arity*. 

**Def:** We can define the set of all finite ground terms you can build using the symbols in $\Sigma$. We do this inductively. For the base case, if $c\in \Sigma$ has arity $0$, then $c\in T_\Sigma$. If $f\in \Sigma$ has arity $n$, and $t_1,\dots, t_n\in T_\Sigma$, then $ft_1\cdots t_n\in T_\Sigma$. 

**Def:** A $\Sigma$-algebra is a structure $\cal A$ consisting of a set $A$, called the *carrier of $\cal A$*, along with a map that assigns to each function $f^\cal A$ or relation $R^\cal A$ of the appropriate arity to each function symbol $f\in\Sigma$ or relation symbol $R\in \Sigma$. 

This interpretation of symbols of $\Sigma$ extends in a natural way by induction to all ground terms. Each ground term $t$ is naturally associated with an element $t^{\cal A} \in A$, defined inductively as follows:$$ft_1\cdots t_n := f^{\cal A}(t_1^{\cal A},\dots, t_n^{\cal A}).  $$This includes the base case: the interpretation of constant $c$ as an element $c^{\cal A}\in A$ is part of the specification of $\cal A$. 

Let $\Sigma$ be an arbitrary signature. The set $T_\Sigma$ of the ground terms over $\Sigma$ gives a family of $\Sigma$-algebras under the following natural interpretation: for $n$-ary $f$, $$f^{T_\Sigma}(t_1,\dots,t_n) := ft_1\cdots t_n.$$This definition includes constants $$c^{T_\Sigma}:= c.$$
The particular algebra depends on the interpretation of the relation symbols of $\Sigma$ as relations on $T_\Sigma$. In such algebras, each ground term $t$ denotes itself $t^{T_\Sigma} = t$. These algebras are called *syntactic* or *term algebras*.

# Automatas

**Def:** Let $\Sigma$ be a signature consisting of finitely many function symbols and a single unary relation symbol $R$. A *deterministic term automaton* ($\sf DTA$) over $\sigma$ is a finite $\Sigma$-algebra.

Let $\cal A$ be a term automaton over $\Sigma$ with carrier $A$. We'll call elements of $A$ *states*. The states satisfying the unary relation $R^\cal A$ will be called the *final states* or *accept states*. Since a unary relation on $A$ is just a subset of $A$, we can write $R^{\cal A}(q)$ or $q\in R^\cal A$ interchangeably. Inputs to $\cal A$ are ground terms over $\Sigma$; that is, elements of $T_\Sigma$.

**Def:** A ground term $t$ is said to be accepted by $\cal A$ if $t^{\cal A}\in R^{\cal A}$. The set of terms accepted by $\cal A$ is denoted is denoted by $L({\cal A})$. A set of terms is called *regular* if it is $L({\cal A})$ for some $\cal A$. 

Let's describe the relationship of this new definition of automata to our previous definitions explain how the old one is a special case of the new one. Given an ordinary $\sf DFA$ over strings $M= (Q, \Sigma, \delta, s, F)$, where $\Sigma'$ is a finite alphabet, let $\Sigma:= \Sigma' := \{\square, R\}$, where $\square, R\notin \Sigma'$. We make $\Sigma$ into a signature by declaring all elements of $\Sigma'$ to be unary function symbols, $\square$ a constant, and $R$ a unary relation symbol. There is a one-to-one correspondence between ground terms over $\Sigma$ and strings $\Sigma'^*$: the string $a_1a_2\cdots a_n\in \Sigma'^*$ corresponds to the ground term $a_n a_{n-1}\cdots a_2a_1\square\in T_\Sigma$.

Now we make a $\Sigma$-algebra out of $M$, which will denote by $\cal M$. The carrier of $M$ is $Q$. The symbols of $\Sigma$ are interpreted as follows:
- $\square^{\cal M} := s$. 
- $a^{\cal M}(q) := \delta(q, a)$,
- $R^{\cal M} := F$. 
In other words, the constant $\square$ is interpreted as the start state of $M$; the symbol $a\in \Sigma'$ is interpreted as the unary function $q\mapsto \delta(q, a)$; and the relation symbol$ is interpreted as the set of final states $F$. We see that$$\hat \delta(s, a_1\cdots a_n) = a_n\cdots a_n \square^{\cal M}.   $$
Therefore, $$a_1\cdots a_n \in L(M) \iff a_n \cdots a_1\square^{\cal M}\in L(\mathcal M).$$

### Homomorphisms

Let $\cal A$ and $\cal B$ be two $\Sigma$-algebras with carriers $A$ and $B$. respectively, A *$\Sigma$-algebra homomorphism* from $\cal A$ to $\cal B$ is a map $\varphi: A \to B$ such that
- for al $n$-ary function symbols $f\in\Sigma$ and all $a_1,\dots, a_n\in A$,$$\varphi(f^{\cal A}(a_1,\dots, a_n)) = f^{\cal B}(\varphi(a_1),\dots, \varphi(a_n));  $$
- for all $n$-ary relation symbols $R\in \Sigma$ and all $a_1,\dots, a_n \in A$, $$R^{\cal A}(a_1, \dots a_n) \iff R^{\cal B}(\varphi(a_1), \dots,\varphi(a_n)).   $$

**Def:** A homomorphism $\varphi: \cal A \to B$ that is surjective is called an *epimorphism*. A homomorphism $\varphi: \cal A \to B$ is injective is called a *monomorphism*. A homomorphism that is both an epimorphism and a monomorphism is called an *isomorphism*. If $\varphi: \cal A \to B$ is an epimorphism then the algebra $\cal B$ is called a *homomorphic image* of $\cal A$. 

**Def:** Let $\Sigma$ be a signature consisting of finitely many functions symbols and a single unitary relation $R$. Let $A\subseteq T_\Sigma$ be an arbitrary set of ground terms, and let $T_\Sigma(A)$ denote the term algebra obtained by interpreting $R$ as the set $A$; that is, $R^{T_\Sigma(A)} =A$. 

**Lemma:** The set $A$ is regular iff the algebra $T_\Sigma(A)$ has finite homomorphic image.

**Def:** Every $\Sigma$-algebra homomorphism $\varphi: \cal A \to B$ induces a certain natural binary relation on $\cal A$: $$u\equiv_\varphi v \stackrel{\text{def}}{\iff} \varphi(u) = \varphi(v).  $$The relation $\equiv_\varphi$ is called the *kernel* of $\varphi$. We see that the kernel of any homomorphism defined on $\cal A$ is an equivalence relation on $\cal A$. 

**Def:** Let $\cal A$ be a $\Sigma$-algebra with carrier $A$. A *congruence* on $\cal A$ is an equivalence relation $\equiv$ on $A$ such that 
- for al $n$-ary function symbols $f\in\Sigma$, if $u_i\equiv_\varphi v_i$,$1\le i \le n$, then $$f^{\cal A}(u_1,\dots, u_n) = f^{\cal A}(v_1,\dots, v_n);  $$
- for all $n$-ary relation symbols $R\in \Sigma$, if $u_i\equiv_\varphi v_i$,$1\le i \le n$, then $$R^{\cal A}(u_1, \dots u_n) \iff R^{\cal A}(v_1, \dots,v_n).   $$
**Lemma:** 
- The kernel of any homomorphism is a congruence.
- Any congruence is the kernel of an epimorphism.

**Def:** Define a *context* to be a term in $T_{\Sigma\cup\{x\}}$, where $x$ is a new symbol of arity $0$. For context $u$ and ground term $t\in T_\Sigma$, denote by $\text s_t^x(u)$ the term in $T_\Sigma$ obtained by substituting $t$ for all occurrences of $x$ in $u$. Formally  $$\begin{align*} \text s_t^x(x) &:= t, \\ \text s_t^x (ft_1\cdots t_n) &:= f\text s_t^x(t_1)\cdots \text s_t^x(t_n).\end{align*}$$
As usual, the last line includes the case of constants: $s_t^x (c) := c$. 

**Def:** Let $\Sigma$ be a signature consisting of finitely many function symbols and a single unary relation $R$. For a given $A\subseteq T_\Sigma$ and ground terms $s,t\in T_\Sigma$, define$$s\equiv_A t \stackrel{\text{def}}{\iff} \text{for all contexts }u, \text s_s^x(u)\in A\iff \text s_t^x(u) \in A.   $$
**Myhill-Nerode Theorem for term Automata:** Let $A\subseteq T_\Sigma$. Let $T_\Sigma(A)$ denote the term algebra over $\Sigma$ in which $R$ is interpreted as the unary relation $A$. The following statements are equivalent:
- $A$ is regular;
- $T_\Sigma(A)$ has a finite homomorphic image;
- there exists a congruence of finite index on $T_\Sigma(A)$;
- the relation $\equiv_A$ is of finite index. 
