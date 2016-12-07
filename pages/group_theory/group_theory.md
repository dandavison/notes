Title: Group Theory
Slug: group-theory
Date: 2016-12-04

$$
\newcommand{\R}{\mathbb{R}}
$$


A group is a set, together with an operation that can be performed on two elements to produce another element.

Concrete examples of groups:

- $\{1, i, -1, -i\}$ where the operation is multiplication of complex numbers.

- $GL_n(\R)$: the set of $n \times n$ matrices, under matrix multiplication.

- $S_2$: the set of permutations of two objects, where the operation is
  composition of functions.  There are just two elements in the group: the
  do-nothing permutation and the switch-the-elements permutation: $\{e,
  \tau\}$.

- $S_3$: the set of permutations of three objects. There are 6 elements: the
  identity, 3 transitions[ref]A transition is a permutation that switches two
  elements and leaves all other alone[/ref] and two cyclic permutations.


Note that in the first two examples, the elements being composed are "inert"
objects (numbers or matrices): they are not themselves functions. However, in
$S_2$ and $S_3$, the *elements* being composed are already function-like
objects (a permutation of $n$ objects is a bijection from the set to itself).

Hang on, is that true? Both multiplication by a complex number, and matrix
multiplication, can be viewed as composition of functions (a complex number
rotates and scales the complex plane, and a matrix is a linear transformation).

A **homomorphism** is a map from one group to another. If it is bijective, it
is an **isomorphism**. If it is bijective and from one group to itself then it
is an **automorphism**.

Note that these concepts are maps from one group to another, i.e. they take in
an element $g \in G$ and output an element $g' \in G'$. The element $g$ may
itself already be a map of sorts (e.g. if it is a permutation in $S_3$, or if
it is a matrix).


### Inverse of an automorphism is an automorphism

[Artin 2.3.11: show that Aut($G$) is a group]

$$
\newcommand{\a}{\alpha}
\newcommand{\ainv}{\alpha^{-1}}
$$

Suppose $\alpha$ is an automorphism that sends $g_1$ and $g_2$ to $g_1'$ and
$g_2'$, respectively.

<img width="300 px" src="/images/group-theory/inverse-of-automorphism-1.png" />

We need to show that $\ainv$ preserves structure, i.e. that

$$
\ainv(g_1'g_2') = \ainv(g_1')\ainv(g_2').
$$



Now, (1) the RHS is $g_1g_2$ by the definition of inverse, and (2) there exist
    some $g_1, g_2$ for which $g_1'g_2' = \a(g_1)\a(g_2)$, since $a$ is an
automorphism and therefore surjective. So we need to show that

$$
\ainv(\a(g_1)\a(g_2)) = g_1g_2.
$$


Since $\a$ is an automorphism, it preserves structure, therefore
$\a(g_1)\a(g_2) = \a(g_1g_2)$. So,

$$
\ainv(\a(g_1)\a(g_2)) = \ainv(\a(g_1g_2)) = g_1g_2,
$$

as required.

----------------------------------------------------------------------------
