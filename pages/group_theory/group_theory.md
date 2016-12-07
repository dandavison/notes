Title: Group Theory
Slug: group-theory
Date: 2016-12-04

$$
\newcommand{\R}{\mathbb{R}}
\newcommand{\C}{\mathbb{C}}
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

A **homomorphism** is a map[ref]"map" is a synonym of "function".[/ref] from
one group to another. If it is bijective, it is an **isomorphism**. If it is
bijective and from a group to itself (i.e. a permutation of the group elements)
then it is an **automorphism**. The critical feature of all these maps is that
they "preserve group structure", i.e. they preserve the relationships among
group elements defined by the group operation. Suppose that they map from group
$G$ to group $G'$. Then the preservation-of-structure criterion is that the map
sends a product $g_1 \circ g_2$ to the product of whatever the separate
elements are sent to:

$$
f(g_1 \circ g_2) = f(g1) \circ f(g_2)
$$

There the composition on the left is happening in $G$ and the composition on
the right is happening in $G'$. (For an automorphism, $G=G'$.)

Note that an element such as $g_1$ that is being sent somewhere by a morphism
may itself already be a map of sorts, e.g. if it is a permutation in
$S_3$. This is potentially confusing, since an automorphism can be thought of
as a permutation of group elements. So an automorphism on $S_3$ is a
permutation of group elements that are themselves permutations of some generic
labeled objects.


### Inverse of an automorphism is an automorphism

[Artin 2.3.11: show that Aut($G$) is a group]

$$
\newcommand{\a}{\alpha}
\newcommand{\ainv}{\alpha^{-1}}
$$

Suppose $\alpha$ is an automorphism that sends $g_1$ and $g_2$ to $g_1'$ and
$g_2'$, respectively.

<img width="300 px" src="/notes/images/group-theory/inverse-of-automorphism-1.png" />

We need to show that $\ainv$ preserves structure, i.e. that when $\ainv$ acts
on an element which is a product, say $g_1'g_2'$, it sends it to the product of
whatever it send the individual factors to:

$$
\ainv(g_1'g_2') = \ainv(g_1')\ainv(g_2').
$$


Firstly, we know that $\ainv(g_1')$ and $\ainv(g_2')$ exist, i.e. some elements
are taken to them by $a$, because $a$ is an automorphism and therefore
surjective. So we'll call those $g_1$ and $g_2$, and the equality we need to
demonstrate has become

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
