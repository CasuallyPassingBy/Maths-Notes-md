---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]], [[Formalisms Equivalent to General Computation]], [[Arithmetic of Natural Numbers]]

The $\lambda$-calculus consists of a set of objects called $\lambda$-terms and some rules of manipulating them. It was originally designed to capture formally the notions of *functional abstraction* and *functional application* and their interactions.

The $\lambda$-calculus has had a profound impact on computing. One see the basic principles of the $\lambda$-calculus at work in the functional programming framework.

In mathematics, $\lambda$-notation is commonly used to represent functions. The expression $\lambda x. E(x)$ denotes a function that on input $x$ computes $E(x)$. To apply this function to an input $y$, we write $(\lambda x. E(x)) y$, then we substitute the $y$ for the variable $x$ in the body $E(x)$ and evaluates the resulting expression. 

# Pure $\lambda$-Calculus

In the *pure* $\lambda$-calculus, there are only variables $\{f, g, x, y,\dots \}$ and operators for $\lambda$-abstraction and application. Syntactic objects called $\lambda$-*terms* are built inductively from these:
- any variables $x$ is a $\lambda$-term;
- If $M$ and $N$ are $\lambda$-terms, then $MN$ is a $\lambda$-tern, functional application ─ think  of $M$ as a function that is about to be applied to the input $N$; and
- If $M$ is a $\lambda$-term and $x$ is a variable, then $\lambda x.M$ is a $\lambda$-term, function abstraction ─ think of $\lambda x. M$ as the function that input $x$ computes $M$.

The operation of application is not associative, and unparenthesised expression are conventionally to the left; thus $MNP$ should be parsed $(MN)P$.

In the pure $\lambda$-calculus, $\lambda$-terms serve both as functions and data. 

Substitution ruled described above is called $\beta$-reduction. Formally, this works as follows. Whenever our $\lambda$-term contains a substerm of the form $(\lambda x. M)N$, we can replace this subterm by the term $\text s_N^x (M)$, where $\text s_N^x(M)$ denotes the term obtained by
- renaming the bound variables of $M$ (those $y$ occuring in the scope of some $\lambda y$) as necessary so that neither $x$ nor any variable $N$ occurs bound in $M$; and
- substituting $N$ for all occurrences of $x$ in the resulting term.

The first step is necessary only to make sure that any free variables $y$ of $N$ will not be inadvertently captured by a $\lambda y$ occurring in $M$ when the substitution is done in the second step. This is the same problem that comes up in the first-order logic. We can rename bound variables in $\lambda$-terms anytime, since their behaviour as functions is not changed. This process of renaming bound variables is officially called *$\alpha$-reduction*. 

We denote $\alpha$- and $\beta$-reduction $\xrightarrow{\,\alpha\,}$ and $\xrightarrow{\,\beta\,}$, respectively. Thus $$(\lambda x. M) N \xrightarrow{\,\beta\, } \text s_N^x(M).  $$
Computation in the $\lambda$-calculus is performed by $\beta$-reducing subterms whenever possible and for as long as possible.

$(*)$ **Church-Rosser property:** If you can reduce $M$ to $N_1$ by some sequence of reductions steps and $M$ and $N_2$ by some other sequence of reduction steps, then there exists a term $P$ such that both $N_1$ and $N_2$ reduce to $P$. 

**Def:** A term is said to be in *normal form* if no $\beta$-reductions apply; that is, if it has no subterms of the form $(\lambda x. M) N$. A normal form corresponds roughly to a halting configuration of a Turing machine. By the Church-Rosser property, if a $\lambda$-term has a normal form, then that normal form is unique up to $\alpha$-renaming. 

## Church Numerals

To simulate the $\mu$-recursive functions in the $\lambda$-calculus, we must first encode the natural numbers as $\lambda$-terms so they can be used in computations. Alonzo Church came up with a nice way to do this. His encoding is known as the *Church numerals:* $$\begin{align*}
\overline 0 &:= \lambda f. \lambda x.x \\
\overline 1 &:= \lambda f. \lambda x.fx \\
\overline 2 &:= \lambda f. \lambda x.f(fx) \\
&\vdots \\
\overline n &:= \lambda f. \lambda x.f^nx \\
 \end{align*}$$where $f^n x$ is the abbreviation for the term $f(f(\cdots (fx)))$ with $n$ copies of $f$. In other words, $\overline n$ represents the function that an input $f$ return the $n$-fold composition of $f$ with itself. The $\overline n$ are all distinct and in normal form. 
  
Using this representation of the natural numbers, the successor function is defined as$$s := \lambda m. \lambda f. \lambda x. f(m fx)  $$
to see that this is correct, try applying it to any $\overline n$: $$
 \begin{align*}
 s\overline n &= (\lambda m.\lambda f. \lambda x. f(mfx) )(\lambda  f. \lambda x. f^n x) \\
 &\xrightarrow{\,\alpha\,} (\lambda  m. \lambda g. \lambda y. g(mgy)) (\lambda f. \lambda x. f^n x) \\
 &\xrightarrow{\,\beta\,} \lambda g. \lambda y.g((\lambda f.\lambda x.f^nx)gy) \\
  &\xrightarrow{\,\beta\,} \lambda g. \lambda y.g((\lambda x.g^nx)y)
 \\
  &\xrightarrow{\,\beta\,} \lambda g. \lambda y.g(g^n y) \\
   &= {\,\beta\,} \lambda g. \lambda y.g^{n+1}y \\
 &\xrightarrow{\,\alpha\,}\lambda f. \lambda x. f^{n+1}x \\
 &= \overline{n+1}.
 \end{align*}  $$
We can define addition as$$ \text{add} := \lambda x.\lambda y. (x s) y.$$
We can also define multiplication as follows $$\text{mult} := \lambda m.\lambda n. \lambda f.  m(nf).$$
## Conditionals

We introduce the following two functions we call this values 'true' $$\mathsf T:= \lambda x.\lambda y. x $$and 'false' $$\mathsf  F:= \lambda x. \lambda y.y$$

It is possible to define logical operations using the representation of the truth values. The $\text{AND}$ function of two arguments can be defined as  $$\land := \lambda x. \lambda y. xy(\lambda u.\lambda v.v)= \lambda x.\lambda y.xy \sf F $$The $\text{OR}$ function of two arguments can de defined as $$\lor := \lambda x.\lambda y. x(\lambda u.\lambda v. u) y := \lambda x.\lambda y.x \mathsf Ty $$Negation of one argument can be defined as $$¬:= \lambda x. x(\lambda u\lambda v.v)(\lambda a.\lambda b.a) = \lambda x.x \sf FT $$
It is very convenient in programming language to have a function which is true is a number is zero and false otherwise. The following function $\sf Z$ complies with this requirement$$\mathsf Z:= \lambda x.x \sf F¬F  $$
A pair $(a,b)$ can be presented in $\lambda$-calculus using the function $$(\lambda z.zab) $$We can extract the first element of the pair from the expression this function to $\sf T$ $$(\lambda z.zab) \mathsf T = \mathsf Tab = a$$and the second applying the function $\sf F$ $$(\lambda z.zab) \mathsf F = \mathsf Fab) = b.$$The following function generates from the pair $(n, n-1)$ the pair $(n+1, n)$: $$\Phi:= (\lambda p.\lambda z.z(sp\mathsf T)(p\mathsf T))  $$The expression $p\sf T$ extracts the first element of the pair $p$. A new pair is formed using the element, which is incremented for the first position of the new pair and just copied for the second position of the new pair. 

The predecessor of a number $n$ is obtained by applying $n$ times the function $\Phi$ to the pair $(\lambda z.z00)$ and then selecting the second member of the new pair: $$\mathsf P:= (\lambda n. n\Phi(\lambda z.00)) \sf F$$Notice that using this approach the predecessor of zero is zero. We can now define proper subtraction to be $x\mathsf P y$. 

With the predecessor function as the building block, we can now define a function which tests if a number $x$ is greater than or equal to a number $y$: $$\mathsf{GE} := (\lambda x.\lambda y. \mathsf Z(x\mathsf Py)) $$We can get also test if a number $x$ is less  than or equal to a number $y$:  $$\mathsf{LE}:= (\lambda x. \lambda y. \mathsf Z(y\mathsf Px)) $$This leads to the following definition of the function $\sf E$ which tests if two numbers are equal:  $$\mathsf E := (\lambda x.\lambda y. \land (\mathsf Z(x\mathsf Py)) (\mathsf Z(y\mathsf Px)))$$Lastly, for the last conditions we can check for strict inequalities $$\mathsf G := (\lambda x.\lambda y. \land (\mathsf Z(x\mathsf Py)) (¬\mathsf Z(y\mathsf Px))) \qquad \mathsf L := (\lambda x.\lambda y. \land (¬\mathsf Z(x\mathsf Py)) (\mathsf Z(y\mathsf Px)))$$

## Recursion

Recursive functions can be defined in the $\lambda$-calculus using a function which calls a function $y$ and the regenerates itself. This can be better understood by considering the following function $\sf Y$:  $$\mathsf Y:= (\lambda y. (\lambda x.y(xx))(\lambda x. y(xx))) $$This function applied to a function $\sf R$ yields:$$\mathsf{YR} := (\lambda x.\mathsf R(xx))(\lambda x. \mathsf R(xx))  $$which further reduced yields: $$\mathsf R((\lambda x.\mathsf R(xx)  (\lambda x. \mathsf R(xx))))  $$but this means $\sf YR = R(YR)$, that is, the function $\sf R$ is evaluated using the recursive call $\sf YR$ as the first argument.

With everything we have implemente Peano's axioms for arithmetic, using only $\lambda$-calculus. 