---
tags:
  - LinearAlgebra/AffineGeometry
---
Subjects: [[Linear Algebra]], [[Affine Geometry]]
Links: [[Vector Spaces]], [[Group Actions]], [[Homogeneous Spaces]], [[Vector Subspaces]]

**Def:** An *affine space* is a set $A$ together with a vector space $\overrightarrow{A}$, and a transitive and free right action of the additive group of $\overrightarrow{A}$  on the set $A$. The elements of the affine space $A$ are called *points*. The vector space $\overrightarrow{A}$ is said to *associated* to the affine space, and its elements are called *vectors, translations* or sometimes *free vectors*.

Explicitly, the definition above means that the action is mapping, generally denoted as an addition. $(a, v) \mapsto a +v$.
- $a + 0 = a$ for all $a\in A$.
- $(a +v)+w = a +(v+w)$  for all $a\in A$ and $v, w\in \overrightarrow{A}$.
- For every $a\in A$, the mapping $\overrightarrow{A} \to A$ such that $v \mapsto a +v$ is a bijection.

The following are important consequences of the properties above.
- For all $v\in \overrightarrow{A}$ , the mapping $A \to A$ such that $a \mapsto a  + v$ is a bijection.
- For every $a, b\in A$, there exists a unique $v\in \overrightarrow{A}$, denoted $b-a$ such that $b = a+v$.

This means that $A$ is a principal homogeneous group of $\overrightarrow{A}$. 

This subtraction has two following properties, called *Weyl's axioms*:
- for any $a\in A$ and $v\in \overrightarrow{A}$, there's a unique point $b\in A$ such that $b -a = v$.
- for all $a,b, c\in A$, it satisfies $(c-b) + (b-a) = c-a$.
Affine spaces can be equivalently defined as a point set $A$, together with a vector space $\overrightarrow{A}$, and a subtraction satisfying Weyl's axioms. 

 **(The parallelogram identity):** for any $a,b, c,d  \in A$, the equalities $b-a = d-c$ and $c-a = d-b$ are equivalent. 

Every vector space  may be considered as an affine space over itself. This means that every element of  may be considered either as a point or as a vector. This affine space is sometimes denoted $(V, V)$ for emphasising the double role of . When considered as a point the zero vector is denoted $o$ or $O$ and called the *origin. *

If $A$ is another affine space over the same vector space, i.e., $V = \overrightarrow{A}$, the choice of any point $a\in A$ define a unique affine isomorphism, which is the identity of $V$ and maps $a$ to $o$. This means that the choice of an origin $a\in A$ allows to identify $A$ with $(V, V)$ up to canonical isomorphism. 

On the other hand, this property allows us to identify the affine space $A$ with the vector space $V$ in which the place of the origin has been forgotten.

**Def:** The *dimension* of an affine space is defined as the *dimension* of the vector space of its translations. An affine space of dimension $1$ is an *affine line*. An affine space of dimension $2$ is an *affine plane*. An affine subspace of dimension $n-1$ is an affine space of dimension $n$ is an *affine hyperplane*. 

# Subspaces

**Def:** An *affine subspace* $B$ of an affine space $A$ is a subset of $A$ such that given a point $a\in B$, the set of vectors $\overrightarrow B := \{b-a\mid b\in  B\}$ is a linear subspace of $\overrightarrow A$. Note that this property doesn't depend on the choice of $a$. Additionally, $B$ is an affine space, which has $\overrightarrow B$ as its associated vector space.

The affine subspaces of $A$ are the subspace of $A$ of the form $a + V$, where $a\in A$ and $V$ is a subspace of $\overrightarrow A$. 

**Def:** The linear subspace with an affine subspace is often called its *direction*, and tow subspace that share the same direction are said to be parallel.

**Prop:** Given a direction $V$, for any point $a\in A$ there is a unique affine subspace of direction $V$, which passes through $a$, namely $a+V$. 

Every translation $A \to A$ of the form $a\mapsto a+v$ maps any affine subspace to a parallel subspace. 

# Euclidean Spaces

**Def:** Let $E$ be an affine space, such that the associated vector space $V$ is a real inner product space of finite dimension, then we say that $E$ is an *Euclidean space*. 

With this in mind we can define a metric on $E$. Let $a, b\in E$, then $$d(a, b) := \|b-a\| = \sqrt{\langle b-a, b-a\rangle}.$$
In Euclidean geometry, the common phrase *affine property* refers to a property that can be proved in affine spaces, that is, it can be proved without using the inner product.