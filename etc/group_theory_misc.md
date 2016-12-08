Title: Group Theory (Misc)
Slug: group-theory-misc
Date: 2016-12-05


The equivalent in linear algebra is: if a linear transformation sends two
vectors to the same place, then one of the vectors can be expressed as the
other plus some vector in the nullspace. I.e. adding a vector from the
nullspace makes no difference to to where you are sent, and furthermore, that
is the only way two vectors can end up being sent to the same place.


-------------------------------------------------------------------------------

<img src="/notes/images/group-theory/fibres-and-congruence-classes.png" />

-------------------------------------------------------------------------------

*The kernel of a homomorphism is a normal subgroup.*

The structure-preserving property means that the element being conjugated
disappears leaving the conjugating elements to cancel each other out:

$$
\varphi(gag^{-1}) = \varphi(g)\varphi(a)\varphi(g^{-1}) = \varphi(g)1\varphi(g)^{-1} = 1
$$

-------------------------------------------------------------------------------

Whether or not a map is a homomorphism, and what its kernel is, depend on what
the group operation in the codomain is. So you can find normal subgroups of a
group $G$ by considering codomains and codomain operations and determining
their kernel.

-------------------------------------------------------------------------------

$A_n$ is a normal subgroup of $S_n$. What is $A_n$? OK it's to do with
permutations and permutation matrices. Read that bit of ch 1.

-------------------------------------------------------------------------------

For finite groups, the following words have basically the same meaning:
- bijective function
- permutation
-

-------------------------------------------------------------------------------

Note that in the first two examples, the elements being composed are numbers or
matrices: they are not themselves functions. However, in $S_2$ and $S_3$, the
*elements* being composed are already function-like objects (a permutation of
$n$ objects is a bijection from the set to itself).

Hang on, is that true? Both multiplication by a complex number, and matrix
multiplication, can be viewed as composition of functions (a complex number
rotates and scales the complex plane, and a matrix is a linear transformation).
