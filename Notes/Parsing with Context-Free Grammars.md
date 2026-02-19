---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Context-Free Grammars]], [[Nondeterministic Pushdown Automata]], [[Deterministic Pushdown Automata]]

One of the most important applications of context-free languages and pushdown automata is compilers. The compiler has to scan a string and determine the syntactic structure of the program. This process is called *parsing*. 

Formally, parsing is the problem of inverting the yield function of a grammar: given $w$, find the parse tree such that $\text{yield}(t) =w$. 

If the grammar is ambiguous, the parsing problem may require constructing multiple parse trees. Recognition remains polynomial, but constructing all parses may require exponential time.

The subroutine of the compiler that parses the input is called the *parser*. Many parsers use a single stack and resemble $\sf DPDA$s. The theory of $\sf DPDA$s and parsing is so well developed that in many instances a parse for a given grammar can be generated automatically.

 Deterministic parsing corresponds to deterministic pushdown automata. Languages that admit linear-time deterministic parsing are precisely the deterministic context-free languages.

If $A$ is nondeterministic $\sf CFL$, or we are not given a $\sf DPDA$ for it, then the problem becomes a little bit more complicated. If $A$ is given by a $\sf CFG$ $G$, we can first convert $G$ to Chomsky normal form. 

Given a string $w = w_1\cdots w_n\in\Sigma^*$, where each $w_i$ is an element fo $\Sigma$, we can use the notation $w_i^j$ to denote the substring $w_i w_{i+1}\cdots w_{j-1}w_j$. 

**Def:** Let $G = (V,\Sigma,  R, S)$ be a $\sf CFG$. The *size* of $G$, denoted by $|G|$, is the sum of the lengths of all productions in $R$. 

**Def:** Let $G = (V,\Sigma,  R, S)$ be a $\sf CFG$, and let $w =w_1w_2\cdots w_n$, $w_i\in \Sigma$. A nonterminal $A\in V$ $\text c$-derives (consistently derives) $w_i^j$ iff the following conditions hold:
- $A\stackrel{*}{\Rightarrow} w_i^j$ and
- $S \stackrel{*}{\Rightarrow} w_1^{i-1}A w_{j+1}^n$. 
Note that these conditions imply that $S \stackrel{*}{\Rightarrow} w$. 

**Def:** A $\text c$-parser is an algorithm that takes a $\sf CFG$ $G = (\Sigma, V, R, S)$ and string $w\in\Sigma^*$ as input and produces output $\mathcal F_{G, w}$ that acts as an oracle about parse information as follows: for any $A\in V$,
- If $A$ $\text c$-derives $w^j_i$, then $\mathcal F_{G, w}(A, i, j) = \text{‘yes'}$. 
- If $A\stackrel{*}{\not\Rightarrow} w_i^j$, then $\mathcal F_{G, w}(A, i, j) = \text{‘no'}$. 
- $\mathcal F_{G, w}$ answers in constant time.

# Cocke-Younger-Kasami Algorithm

There is an important algorithm due to Cocke, Kasami, and Younger that runs in cubic time. It determines for each substring $y$ of $x$ the set of all nonterminals that generate $y$. This is done inductively on the length of $y$. 

The standard version of $\sf CYK$ operates only on context-free grammars given in Chomsky normal form. Since every context-free grammar can be transformed into a Chomsky normal that is equivalent we can suppose without loss of generality. 

Let $n$ be the length of the string. Draw $n+1$ vertical lines separating the letters and number them form $0$ to $n$. For $0\le i < j \le n$, let $x_{ij}$ denote the substring of $x$ between the lines $i$ and $j$. We build a table $T$ with $n\choose 2$ entries, one for each $i, j$ such that $0\le i < j\le n$. The $i, j$th entry of $T$, denoted $T_{ij}$ refers to the substring $x_{ij}$. 

### Algorithm in Psuedocode

**for** $i:= 0$ **to** $n-1$ **do**
	**begin**
		$T_{i, i+1} :=\varnothing$;
		**for** $A \to a$ a production of $G$ **do**
			**if** $a = x_{i,i+1}$ **then** $T_{i, i+1} := T_{i, i+1}\cup\{A\}$
	**end;**

**for** $m := 2$ **to** $n$ **do**
	**for** $i := 0$ **to** $n-m$ **do**
		**begin**
			$T_{i, i+m} := \varnothing$;
			**for** $j := i+1$ **to** $i+m-1$ **do**
				**for** $A\to BC$ a production of $G$ **do**
					**if** $B\in T_{i,j}\land C\in T_{j, i+m}$ **then** $T_{i, i+m} := T_{i, i+m} \cup \{A\}$
		**end;**

```python

from collections import defaultdict

def cyk_parse(x: str, grammar:dict):
    """
    CYK parsing table builder.

    x: input string (a sequence of terminals)
    grammar: dict mapping nonterminals to list of productions
             where each production is a tuple of symbols.
             Example:
               {
                 "S": [("A","B")],
                 "A": [("a",)],
                 "B": [("b",)]
               }
    """
    n = len(x)
    # T is a 2D table T[i][j] is  set of nonterminals deriving x[i: j]
    T = [[set() for _ in range(n+1)] for _ in range(n+1)]
    
    for i in range(n):
	    for A, prods in grammar.items():
		    for prod in prods:
			    # if it is terminal production A → a
			    if len(prod) == 1 and prod[0] == x[i]:
				    T[i][i+1].add(A)
				    
	# Fill table for lengths m = 2, ..., n
    for m in range(2, n+1):
        for i in range(n-m+1):
            j = i + m
            # For each possible split point
            for k in range(i+1, j):
                for A, prods in grammar.items():
                    for prod in prods:
                        # Only check binary rules A -> B C
                        if len(prod) == 2:
                            B, C = prod
                            if (B in T[i][k]) and (C in T[k][j]):
                                T[i][j].add(A)

    return T
    
grammar = {
    "S": [("A", "B")],
    "A": [("a",)],
    "B": [("b",)]
}

table = cyk_parse("ab", grammar)
for i in range(len(table)):
    for j in range(len(table[i])):
        if table[i][j]:
            print(f"T[{i},{j}] = {table[i][j]}")    

```

The worst case running time of $\sf CYK$ is $\Theta(n^3\cdot |G|)$, where $n$ is the length of the parsed string and |G| is the size fo the $\sf CNF$ grammar $G$. This makes it one of the simplest cubic-time algorithms for recognizing arbitrary context-free languages

CYK as presented solves the recognition problem and provides membership and structural information, but does not by itself reconstruct a parse tree unless backpointers are stored.

### Generalisations

In 1975, Valiant gave an extension of the $\sf CYK$ algorithm. His algorithm computes the same parsing table as the $\sf CYK$ algorithm; yet he showed that algorithms for efficient boolean matrix multiplication can be utilized for performing this computation. 

Using the [[Coppersmith-Winogard Algorithm]] for multiplying these matrices, this gives an asymptotic worst-case running time $O(n^{2.38}\cdot |G|)$. However, the constant term hidden in the big $O$ notation is so large that the Coppersmith–Winograd algorithm is only worthwhile for matrices that are too large to handle on present-day computers and this approach requires subtraction and so is only suitable for recognition. }

Valiant showed that general CFG parsing reduces to Boolean matrix multiplication. Later, Lee showed that any sufficiently subcubic parser implies a subcubic Boolean matrix multiplication algorithm. In 2002, Lillian Lee proved that any parser for context-free grammars working in time $O(n^{3-\varepsilon}\cdot|G|)$ can be effectively converted into an algorithm computing $(n\times n)$ boolean matrices in time $O(n^{3-\varepsilon/3})$. 