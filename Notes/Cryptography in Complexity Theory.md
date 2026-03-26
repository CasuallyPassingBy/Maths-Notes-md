---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]], [[The Complexity Class P]], [[The Complexity Class NP]]

The practice of encryption, using secret codes for private communication, dates back thousand of years. 

The field of cryptography now extends well beyond secret codes for private communication and addresses a broad range of issues concerning the security of information. We now have the ability to digitally sign messages to authenticate the identity of the sender; and to construct new kinds of secret codes that do not require the communicators to agree in advance on the encryption and decryption algorithms.

Cryptography is an important practical application to complexity theory. 

# Secret Keys

When a sender wants to encrypt a message so that only a certain recipient could decrypt it, the sender and receiver share a *secret key*. The secret key is a piece of information that is used by the encrypting and decrypting algorithms. Maintaining the secrecy of the key is crucial to the security of the code because any person with access to the key and encrypt and decrypt messages.

A key that is too short may be discovered through a brute-force search of the entire space of possible keys. The only way to get perfect cryptographic security is with keys that are as long as the combined length of all messages then.

A key that is long as the combined message length is called a *one-time pad*. Essentially, every bit of a one-time pad key is used just once to encrypt a bit of the message, and then that bit of the key is discarded. The main problem with one-time pads is that may be rather large if a significant amount of communication is anticipated. For most purposes, one-time pads are too cumbersome to be considered practical. 

A cryptographic code that allows an unlimited amount of secure communication with keys of only moderate length is preferable. Such codes can't exist in principle but paradoxically are used in practice. This type of code can't exists in principle because a key that is significantly shorter that the combined message length can be found by a brute-force search through the space of possible keys. Therefore a code that is based on such keys is breakable in theory. Of course, if the code could be broken in some other, fast way, it is insecure and shouldn't be used. The difficulty lies in being sure that the code can't be broken quickly.

We currently have no way of ensuring that a code with moderate length keys is actually secure. To guarantee that a code can't be broken quickly, we'd need a proof that finding the key can't be done quickly. Such proofs seem beyond the capabilities of modern mathematics. 

Verifying correctness is easily done by inspecting the messages that have been decrypted with it. Therefore the key verification problem can be formulates as to be in $\sf P$. If we could prove that keys can't be found in polynomial time, we would achieve a major mathematical advance by proving that $\sf P$ is different from $\sf NP$.

One problem that is generally to be difficult for the average case is the problem of integer factorisation. Top mathematicians have been interested in factorisation in centuries, but no one has yet discovered a fast procedure for doing so.

# Public-Key Cryptography

Even when cryptographic keys are moderately short, their management presents an obstacle to their widespread use in conventional cryptography. One problem is that pair of parties that desires private communication needs to establish a joint secret key for this purpose. Another problem is that each individual needs to keep a secret database of all keys that have been so established.

The recent development of public-key cryptography provides an elegant solution to both problems. Separating two keys, one for encryption and the other for decryption, separating the two keys has profound consequences. Now each individual only needs to establish a single pair of keys: an encryption key $E$ and a decryption key $D$. The individual keeps $D$ secret but publicises $E$. If another individual wants to send a them a message, they look up $E$ in the public directory, encrypts the message with it, and sends it to them. The first individual is the only who knows $D$, so only he can decrypt that message.

# One-Way Functions

A function $f: \Sigma^* \to\Sigma^*$ is *length-preserving* if the lengths of $w$ and $f(w)$ are equal for every $w$. A length-preserving function is a *permutation* if it is injective.

Let's say that a probabilistic Turing machine $M$ computes a *probabilistic function* $M: \Sigma^* \to \Sigma^*$, where, if $w$ is an input and $x$ is an output, we assign $$P[M(w) = x] $$to be the probability that $M$ halts in an accept state with $x$ on its tape when it is started on input $w$. Note that sometimes fail to accept on $w$, so $$\sum_{x\in \Sigma^*} P[M(w) = x] \le 1. $$
**Def:** A *one-way permutation* is a length-preserving permutation $f$ with the following properties.
1. It is computable in polynomial time.
2. For every probabilistic polynomial time Turing machine $M$, every $k$, and sufficiently large $n$, if we pick a random $w$ of length $n$ and run $M$ on input $w$, $$P_{M, w}[M(f(w)) = x] \le n^{-k}. $$Here $P_{M, w}$ means that the probability is taken over the random choices made by $M$ and the random selection of $w$.

A *one-way function* is a length-preserving function $f$ with the following two properties.
1. It is computable in polynomial time.
2. For every probabilistic polynomial time Turing machine $M$, every $k$, and sufficiently large $n$, if we pick a random $w$ of length $n$ and run $M$ on input $w$, $$P[M(f(w)) = y \text{ where } f(y) = f(w)] \le n^{-k}. $$
For one-way permutations, any probabilistic time algorithm has only a small probability of inverting $f$; that is, it is unlikely to compute $w$ from $f(w)$. For one-way functions, any probabilistic polynomial time algorithm is unlikely to be able to find any $y$ that maps to $f(w)$.

If we assume the existence of one-way functions, we may construct a private key-cryptosystem that is provably secure. 
# Trapdoor Functions

We don't know whether the existence of a one-way function alone is enough to allow the construction of a public-key cryptosystem. To get such a construction we use a related object called a *trapdor function*, which can be efficiently inverted in the presence of special information.

If we have a family of fucntions $\{f_i\mid i \in \Sigma^*\}$, we can represent them by a single function $f: \Sigma^* \times \Sigma^*\to \Sigma^*$, where $f(i, w) := f_i(w)$ for any $i$ and $w$. We call $f$ an indexing function. Say that $f$ is length-preserving if each of the indexed functions $f_i$ is length-preserving.

**Def:** A *trapdoor function* $f: \Sigma^*\times\Sigma^* \to \Sigma^*$ is a length-preserving indexing function that has an auxiliary probabilistic time Turing machine $G$ and auxiliary function $h: \Sigma^*\times\Sigma^*\to \Sigma^*$. The trio $f, G$ and $h$ satisfy three conditions.
1. Functions $f$ and $h$ are computable in polynomial time.
2. For every probabilistic polynomial time Turing machine $E$ and every $k$ and sufficiently large $n$, if we take a random output $\langle i, t\rangle$ of $G$ on $1^n$ and a random $w\in\Sigma^n$ then $$P[E(i, f_i(w)) = y, \text{ where } f_i(y) = f_i(w)] \le n^{-k}.$$
3. For every $n$, every $w$ of length $n$, and every output $\langle i, t\rangle$ of $G$ that occurs with nonzero probability for some input to $G$ $$h(t, f_i(w)) = y, \text{ where } f_i(y) = f_i(w).$$
The probabilistic Turing machine $G$ generates an index $i$ of a function in the index family while simultaneously generating a value $t$ that allows $f_i$ to be inverted quickly. Condition $2$ says that $f_i$ is hard to invert in the absence of $t$. Condition $3$ says that $f_i$ is easy to invert when $t$ is known. Function $h$ is the inverting function.
