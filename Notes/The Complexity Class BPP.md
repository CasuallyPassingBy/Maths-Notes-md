---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Probabilistic Algorithms in Complexity Theory]], [[The Complexity Class P]], [[The Complexity Class PSPACE]], [[Branching Programs in Complexity Theory]]

**Def:** A *probabilistic Turing machine* $M$ is a type of nondeterministic Turing machine in which each nondeterministic step is called *coin-flip step* and has two legal moves. We assign a probabilisty to each branch $b$ of $M$'s computation on input $w$ as follows. Define the probability of branch $b$ to be  $$P(b) := 2^{-k},$$where $k$ is the number of coin-flips steps that occur on branch $b$. Define the probability that $M$ accepts $w$ to be $$P(M \text{ accepts }w) = \sum_{\substack{b \text{ is an } \\ \text{accepting branch}}} P(b). $$
In other words, the probability that $M$ accepts $w$ is the probability that we would reach an accepting configuration if we simulated $M$ on $w$ by flipping a coin to determine which move to follow at each coin-flip step. We let   $$P(M \text{ rejects }w) = 1-P(M \text{ accepts }w).$$
When a probabilistic Turing machine recognise a language, it must accept all strings in the language and reject all strings out of the language as usual, except that we allow the machine a small probability of error. For $0 \le \varepsilon < \frac12$ we say that $M$ recognises language $A$ with error probability $\varepsilon$ if
1. $w\in A$ implies $P(M \text{ accepts }w) \ge 1-\varepsilon$, and
2. $w\notin A$ implies $P(M \text{ rejects }w) \ge 1-\varepsilon$.

In other words, the probability that we would obtain the wrong answer by simulating $M$ is at most $\varepsilon$. We also consider error probability bounds that depend on the input length $n$. 

We are interested in probabilistic algorithms that run efficiently that run efficiently in time and/or space. We measure the time and space complexity of a probabilistic Turing machine, by using the worst case computation branch on each input.

**Def:** $\sf BPP$ is the class of languages that are recognised by probabilistic polynomial time Turing machines with en error probability of $\frac13$.

**Amplification Lemma:** Let $\varepsilon \in (0, \frac12)$.  Then for any polynomial $p(n)$ of a probabilistic polynomial time Turing machine $M_1$ that operates with error probability $\varepsilon$ has an equivalent probabilistic polynomial time Turing machine $M_2$ that operates with an error probability of $2^{-p(n)}.$ 

We define this class with an error probability of $\frac13$, but any constant error would yield the an equivalent definition as long as it is strictly between $0$ and $\frac12$. 

In our analyses, we assume that these algorithms are implemented using true randomness. True randomness may be difficult/impossible to obtain, so it is usually simulated with *pseudorandom generators*, which are deterministic algorithms whose output appears random. Algorithms that are designed to use randomness may work equally work will with these pseudorandom generators, but proving that they do is generally more difficult. Indeed, sometimes probabilistic algorithms may not work well with certain pseudorandom generators. Sophisticated pseudorandom generators have been devised that produce results indistinguishable from truly random results by any test that operates in polynomial time, under the assumption that a [[one-way function]] exists. 

**Prop:** $\sf BPP \subseteq PSPACE$. 

**Def:** Let $\sf BPL$ be the collection of languages that are decided by probabilistic log space Turing machine with error probability $\frac13$. 

**Prop:** $\sf BPL \subseteq P$.

## Primality

We can think of [[Fermat's Little Theorem]] as providing a test for primality called a *Fermat test*. when we say that $p$ passes the Fermat test at $a$, we mean that $a^{p-1} \equiv 1 \pmod p$. the theorem states that the primes pass all Fermat tests for $a\in (\Bbb Z/p\Bbb Z)\setminus\{0\}$.

We call a number a [[Fermat's Little Theorem#^e7327a|pseudoprime]] if it passes Fermat tests for all smaller $a$ relatively prime to it. With the exception of the infrequence [[Fermat's Little Theorem#^6e0492|Carmichale numbers]], which are composite yet pass all Fermat tests, the pseudoprime numbers are identical to the prime numbers. We begin by giving a very simple probabilistic polynomial time algorithm that distinguishes primes from composites except for the Carmichael numbers. 

A psuedoprimality algorithm that goes through all Fermat tests would require exponential time. 

**Prop:** For any integer $p>1$, if $p$ isn't psuedoprime, then $p$ fails the Fermat test for at least half of all numbers in $\Bbb Z/p\Bbb Z$. 

The algorithm works by trying several tests chosen at random. If any fail, the number must be composite. The algorithm contains a parameter $k$ that determines the error probability.

$\text{Pseudoprime} =$ "On input $p$:
1. Select $a_1,\dots, a_k$ randomly in $(\Bbb Z/p\Bbb Z)\setminus\{0\}$.
2. Compute $a_i^{p-1}\pmod p$ for each $i$.
3. If all computed values are $1$, accept; otherwise, reject."

If $p$ is prime, it passes all tests and the algorithm accepts with certainty. If $p$ isn't psuedoprime, it passes at most half of all tests. In that case it passes each randomly selected with probability at most $\frac12$. The probability that it passes all randomly slected tests is thus at most $2^{-k}$.  We see that polynomial time because modular exponentiation is computable in polynomial time.

We want to convert our psuedoprime detector to a primality detector. We know that in $(\Bbb Z/p\Bbb Z)$ the number $1$ has exactly two roots when $p$ is a prime and $p \ne 2$. For many composite numbers, including all the Carmichael numbers, $1$ has more than $2$ square roots. If a number passes the Fermat tests at $a$, the algorithm finds one of its square roots of $1$ at random and determines whether the square root is $\pm 1$. If it isn't, we know that the number isn't prime.

We can obtain square roots of $1$ if $p$ passes the Fermat test at $a$ because $a^{p-1}\equiv 1 \pmod p$, and so $a^{(p-1)/2}$ is a square root of unity. If the value is still $1$ we may repeatedly divide the exponnent by two, so long as the resulting exponent remains an integer, and see whether the first number that is different from $\pm 1$ or some other number. 

$\text{Prime} =$ " On input $p$:
1. If $p$ is even, accept if $p = 2$; otherwise, reject.
2. Select $a_1,\dots, a_k \in (\Bbb Z/p\Bbb Z)\setminus\{0\}$.
3. For each $i$ from $1$ to $k$:
	1. Compute $a_i^{p-1}\pmod p$ and reject if different from $1$.
	2. Let $p-1 = st$, where $s$ is odd and $t = 2^h$ is a power of $2$.
	3. Compute the sequence $a_i^{s\cdot 2^0},a_i^{s\cdot 2^1}, \dots, a_i^{s\cdot 2^h} \pmod p$.
	4. If some element of this sequence is not $1$, find the last element that is not $1$ and reject if that element is not $-1$.
4. All tests have passed at this point, so accept."

This is the **Miller-Rabin Primality Test.**

**Lemma:** If $p$ is an odd prime number, then $P(\text{Prime accepts } p) = 1$. 

**Lemma:** If $p$ is an odd composite number, $P(\text{Prime rejects } p) \le 2^{-k}$. This proof uses [[Linear Congruences#Chinese Remainder Theorem|the Chinese remainder theorem]].

**Th:** Let $\text{Primes} := \{n \mid n \text{ is a prime number in binary}\}$. We know that $\text{Primes} \in \sf BPP$. 

Note that the probabilistic primality algorithm has *one-sided error.* When the algorithm outputs *reject*, we know that the input must be composite. When the output is accept, we know only that the input could be prime or composite. Thus an incorrect answer only occur when the input is a composite number. The one-sided error feature is common to many probabilistic algorithms, so they have a special complexity class. 

**Def:** $\sf RP$ is the class of languages that are recognised by probabilistic time Turing machines where inputs in the language are accepted with a probability of at least $\frac12$ and inputs not in the language are rejected with a probability of $1$. 

**Th:** Let $\text{Composites} := \{n \mid n \text{ is a composite number in binary}\}$. We know that $\text{Composite} \in \sf RP$. 

**Prop:** If $\sf NP \subseteq BPP$, then $\sf NP = RP$. 

**Def:** A $\sf ZPP$-machine to be a probabilistic Turing machine which is permitted three types of output on each of its branches: accept, reject, and $?$. A $\sf ZPP$-machine $M$ decides a language $A$ if $M$ outputs the correct answer on every input string $w$, accept if $w\in A$ and reject if $w\notin A$, with probability $\frac 23$, and $M$ never outputs the wrong answer. On every input, $M$ may output $?$ with probability at most $\frac 13$. Furthermore, the average running time over all branches of $M$ on $w$ most be bounded by a polynomial in the length of $w$.

**Prop:** $\sf RP \cap coRP = ZPP.$

# Other Problems in BPP

Let $$\text{EQ}_\mathsf{ROBP} := \{\langle B_1, B_2\rangle \mid \text{$B_1$ and $B_2$ are equivalent read-once branching program}\}.$$
**Th:** $\text{EQ}_\mathsf{ROPB}$ is in $\sf BPP$. 