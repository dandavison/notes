Title: Harvard E222 Algebra - Homework
Slug: harvard-e222
Date: 2016-12-08

$$
\newcommand{\Z}{\mathbb{Z}}
\newcommand{\R}{\mathbb{R}}
\newcommand{\C}{\mathbb{C}}
\newcommand{\mat}[4]{\begin{bmatrix}#1 & #2\\#3 & #4\\ \end{bmatrix}}
\newcommand{\smat}[4]{\tiny{\mat{#1}{#2}{#3}{#4}}}
\newcommand{\cvec}[2]{\begin{pmatrix}#1\\#2\end{pmatrix}}
\newcommand{\scvec}[2]{\tiny{\cvec{#1}{#2}}}
\newcommand{\GL}{\mathrm{GL}}
\newcommand{\GLR}[1]{\mathrm{GL}_{#1}(\R)}
\newcommand{\GLC}[1]{\mathrm{GL}_{#1}(\C)}
\newcommand{\1}{{-1}}
$$

Exercises from Artin *Algebra* 1st edition.

- [Harvard E122](http://wayback.archive-it.org/3671/20150528171650/https://www.extension.harvard.edu/open-learning-initiative/abstract-algebra)
- [Harvard 122](http://www.math.harvard.edu/~ctm/home/text/class/harvard/122/02/html/hw.html)

----------------------------------------------------------------------------

### E122 Homework 1

** 1. Read 1.1, pp. 38-42 **

** 1.1.7 **

** 1.1.16 **

** 1.1.17 **

----------------------------------------------------------------------------
### E122 Homework 2
**Read 2.1, 2.2**

** 2.1.5 **

** 2.1.7 **

** 2.2.1 **

** 2.2.14 (122) Let $G$ be a cyclic group of order $n$, and let $r$ be an integer
dividing $n$. Prove that $G$ contains exactly one subgroup of order $r$. **

If $n$ is prime then the only subgroups of $G$ are $\{e\}$ and $G$. The
integers which divide $n$ are 1 and $n$ and so it is true that for every such
integer $r$ there is one subgroup of order $r$.

If $n$ is not prime then $G$ has non-trivial subgroups for every integer that
divides it.

For example, if $G$ has order 8, the claim is that $G$ has only one subgroup of
order 2. Well, all subgroups of order 2 are isomorphic to $\{e, \tau\}$. So the
claim implies that groups of permutations of order 4, 6, 8 etc (i.e. $S_4, S_6,
S_8$) contain only one transposition.


A solution is given in the
[Harvard 122 materials](http://www.math.harvard.edu/~ctm/home/text/class/harvard/122/02/html/home/solns/hw2.pdf).

The starting point is to note that $<g^{n/r}>$ is a subgroup of order $r$
($n/r$ fits $r$ times into each chunk of $n$ items). So in the example with $G$
of order 8, $<g^{4}>$ has order 2. The question is whether there is any other
subgroup of order 2. Intuitively it seems obvious that the answer is no, since
only 4 divides up chunks of 8 in that way.

Formally, the proof proceeds by supposing that $H' = <g^m>$ also has order $r$
(using a lemma that every subgroup of a cyclic group is cyclic). It then shows
that $m$ must divide $n$ (otherwise leads to a contradiction). Therefore the
order of $H'$ is $n/m$. Therefore $m = n/r$ which shows that $H'$ is $H$.

** 2.2.15 **

** 2.2.20(a) **


----------------------------------------------------------------------------

### E122 Homework 3

** 2.3.1 **

** 2.3.11 **

** 2.3.12 **

** 2.4.3 **

** 2.4.5 (122) **

** 2.4.6 **

** 2.4.8 (122) **

** 2.4.11 **

** 2.4.16 (122) **

** 2.4.23 (122) **


----------------------------------------------------------------------------
### E122 Homework 4
** 1. Read Artin 1.4.**

** 2. Let $V$ denote the Klein 4-group. Show that Aut($V$) is isomorphic to $S_3$.**

Every automorphism sends the identity to itself. This is because an
automorphism must preserve structure, therefore we require $\rho(e) =
\rho(ee^\1) = \rho(e)\rho(e^\1) = \rho(e)\rho(e)^\1$ which implies $\rho(e) =
e$.

Therefore, elements of Aut($V$) are distinguished by their effect on the 3
non-identity elements and there is a 1-1 correspondence $f$ between elements of
Aut($V$) and $S_3$.

We need to show that $f$ is a homomorphism, i.e. that $f(\rho_1 \rho_2) =
f(\rho_1) f(\rho_2)$. The operation is composition of permutations in both
groups...the identity seems obvious.

**3.**

Define $f : \GL_n(\R) \rightarrow \GL_n(\R)$ by $f(A) =~ ^tA^\1$ (where $^tA$
is the transpose of $A$). Show that $f$ is an automorphism, but not an inner
automorphism for $n ≥ 1$.

To show that $f$ is an automorphism we need to show that it preserves structure
and is a bijection.

*Preservation of structure:* We require that $^t(AB)^\1 =~ ^tA^\1~ ^tB^\1$.
The RHS is $^tA^\1~ ^tB^\1 = (^tB^tA)^\1 = ~^t(AB)^\1$ as required.

*Bijection:* $f^\1(A) =~ ^tA$. Since an inverse mapping exists, the original
mapping must be bijective.

Finally, we need to show that $f$ is not an inner automorphism for $n \geq
1$. An inner automorphism is an automorphism defined by $\rho(A) = BAB^\1$ for
some fixed $B$. So we need to show that there is no $B$ for which $^tA^\1 =
BAB^\1$ for all $A$. $BAB^\1$ corresponds to the action of $A$ performed in a
basis defined by $B$. The determinant of $A$ is invariant under change of
basis. However, $\det ~^tA^\1 = (\det A)^\1$. Therefore $^tA^\1 = BAB^\1$ is
not true in general since it is not true when $\det A \neq \pm 1$.

http://math.stackexchange.com/questions/98378/fx-tx-1-is-an-automorphism-of-gl-n-mathbbr

I'm also watching these lectures and trying to do the homework, so by no means
an expert. In the final part of the proof, a variant would be to use
determinants:

Assume that $f$ is an inner automorphism. Therefore for some fixed $B$, $^tA^\1
= BAB^\1$ for all $A$. But this implies $(\det A)^\1 = \det A$ which is true
only for $\det A = \pm 1$. Therefore $f$ is not an inner automorphism.


**4. 1.4.5 Prove that the transpose of a permutation matrix P is its inverse.**

### E122 Homework 5
----------------------------------------------------------------------------

**2.5.1 Prove that the nonempty fibres of a map form a partition of the domain.**

We need to show

1. That every element of the domain is in some fibre, and
2. That no element is in more than one fibre

Let $f$ be a map from set $S$ to set $T$. A fibre $\phi_t$ of $f$ is the set
$\{s: f(s) = t\}$.

For any element $s$ in the domain, $f(s)$ exists and $s$ is in fibre
$\phi_{f(s)}$. This proves (1).

To prove (2), suppose that $s$ belongs to fibres $\phi_{t_1}$ and
$\phi_{t_2}$. Then $f(s) = t_1$ and $f(s) = t_2$ which is a contradiction
showing that no element belongs to two fibres.

----------------------------------------------------------------------------

**2.5.6**

**(a) Prove that the relation $x$ conjugate to $y$ in a group $G$ is an
  equivalence relation on $G$.**

$x$ conjugate to $y$ means $y = gxg^{-1}$ for some $g \in G$. We need to show
that the relation is reflexive, transitive and symmetric.

*Reflexivity*: $x$ is equal to $x$ conjugated with the identity element: $x = exe^{-1}$.

*Symmetry*: Let $y = gxg^{-1}$. Then multiplying on the right by $g$ and on the
            left by $g^{-1}$ gives $g^{-1}yg = x$.

*Transitivity*: Let $y = g_1xg_1^{-1}$ and $z = g_2yg_2^{-1}$. Then $z =
                g_2(g_1xg_1^{-1})g_2^{-1} = (g_2g_1)x(g_1^{-1}g_2^{-1})$


**(b) Describe the elements $a$ whose conjugacy class (= equivalence class)
consists of the element $a$ alone.**

----------------------------------------------------------------------------

**2.6.2 Prove directly that distinct cosets do not overlap.**

Let $H$ be a subgroup of $G$ and let $g_1H = \{g_1h:h\in H\}$ be a coset of $H$
in $G$. Consider an element $g_3 \in g_1H$. This means that $g_3 = g_1h$ for a
unique $h \in H$.

Suppose that $g_3$ is also in another coset $g_2H$. Then $g_3 = g_1h = g_2h'$
for $h, h' \in H$ and therefore $g_1hh'^{-1} = g_2$. But $hh'^{-1} \in H$ so
$g_2$ is in coset $g_1H$, which shows that cosets $g_1H$ and $g_2H$ are the
same.

----------------------------------------------------------------------------

**2.6.4 Give an example showing that left cosets and right cosets of $\GL_2(\R)$
  in $\GL_2(\C)$ are not always equal.**

We don't even need to consider matrices outside $\GL_2(\R)$. Let A =
$\smat{1}{0}
      {0}{0}$ and let $H = \GL_2(\R)$.

Geometrically, this matrix projects points in 2D onto the x-axis.

The left coset of $\GL_2(\R)$ containing $A$ is the set of matrices of the form

$$
\smat{1}{0}
     {0}{0} \smat{a}{b}
                 {c}{d} = \smat{a}{b}
                               {0}{0}
$$

where $a,b,c,d \in \R$. Geometrically, this composition first sends the basis
vectors to new locations with x-coordinates $a$ and $b$, and then projects onto
the x axis.

The right coset of $\GL_2(\R)$ containing $A$ is the set of matrices of the form

$$
\smat{a}{b}
     {c}{d} \smat{1}{0}
                 {0}{0} = \smat{a}{0}
                               {c}{0}
$$

Geometrically, this composition first sends the $\scvec{0}{1}$ basis vector to
the origin, and then performs an arbitrary linear transformation. But once sent
to the origin, the $\scvec{0}{1}$ basis vector stays there, regardless of the
nature of the second transformation.

----------------------------------------------------------------------------

**2.6.5 Let $H$, $K$ be subgroups of a group $G$ of orders 3, 5
  respectively. Prove that $H \cap K = \{e\}$.**

Since $H$ and $K$ are of prime order, they are isomorphic to the cyclic groups
of orders 3 and 5 respectively. Therefore the non-identity elements of $H$ are
of order 3, and the non-identity elements of $K$ are of order 5 (because the
order of an element in a group must divide the order of the group). Therefore,
while $e$ is in $H \cap K$, no other element is.

----------------------------------------------------------------------------


** 2.6.10 (122) **

** 2.6.11 (122) **

** 2.8.2 (122) **

** 2.8.10 (122) **


### E122 Homework 6

----------------------------------------------------------------------------
** 2.9.2 2. **

** (a) Prove that the square $a^2$ of an integer $a$ is congruent to 0 or 1 modulo 4. **

Suppose $a$ is even, so $a = 2n$ for some $n \in \Z$. Then $a^2 = 4n^2 \equiv
0$ (mod 4). Alternatively, suppose $a$ is odd, i.e. $a = 2n + 1$ for some $n
\in \Z$. Then $a^2 = 4n^2 + 4n +1 \equiv 1$ (mod 4).

** (b) What are the possible values of $a^2$ modulo 8? **

If $a$ is even, then $a^2 = 4n^2$. If $n^2$ is odd then $a^2 \equiv 4$ (mod 8)
and if even then $a^2 \equiv 0$ (mod 8). If $a$ is odd, then $a^2 = 4n(n+1) + 1
\equiv 1$ (mod 8). So the possible values are 0, 1, 4.


----------------------------------------------------------------------------

** 2.9.4 Prove that every integer a is congruent to the sum of its decimal
digits modulo 9. **

Let $a = d_0 + d_1 10 + d_2 10^2 + \ldots$.

[*Good solution*](https://github.com/AMouri/artin-algebra/blob/3083860baf553b472495fd01ef62489db9a261ee/Chapter%202%20-%20Groups/Section%209%20-%20Modular%20Arithmetic/solutions.tex#L47):
Note that $10 \equiv 1$ (mod 9). So $a \equiv d_0 + d_1 + d_2 + \ldots$ (mod 9).

*My solution*: we require that the difference is a multiple of 9. The difference
is $\sum_{i=0}^\infty d_i 10^i - \sum_{i=0}^\infty d_i = \sum_{i=0}^\infty
d_i(10^i - 1)$...which is a multiple of 9.


----------------------------------------------------------------------------

** 2.9.5 Solve the congruence $2x \equiv 5$ **

** (a) modulo 9 **

[*Good solution*](https://github.com/AMouri/artin-algebra/blob/3083860baf553b472495fd01ef62489db9a261ee/Chapter%202%20-%20Groups/Section%209%20-%20Modular%20Arithmetic/solutions.tex#L52):
$x = 2^\1 5 \equiv 5 \cdot 5 \equiv 7$ (mod 9)

The possible values of $2x$ (mod 9) are 0, 2, 4, 6, 8, 1, 3, 5, 7, 9. So 2 (mod
9) does have a multiplicative inverse (5).


*My solution*: $14 = 2 \cdot 7 \equiv 5$ (mod 9). So the solution is $x \equiv 7$ (mod 9).

** (b) modulo 6 **
[*Good solution*](https://github.com/AMouri/artin-algebra/blob/3083860baf553b472495fd01ef62489db9a261ee/Chapter%202%20-%20Groups/Section%209%20-%20Modular%20Arithmetic/solutions.tex#L54)
The possible values of $2x$ (mod 6) are 0, 2, 4. Therefore $2x \equiv 5$ has no
solution.

I.e. 2 (mod 6) has no multiplicative inverse?

*My solution*: $\bar 5$ (mod 6) $= 5 + 6\Z = 1 + 2\cdot2 + 2\cdot3\Z = 1 + 2(2 + 3\Z)$ is an
equivalence class of odd numbers. Therefore $2x \equiv 5$ (mod 6) has no
solutions.



----------------------------------------------------------------------------

**2.9.8 Use Proposition (2.6) to prove the Chinese Remainder Theorem: Let $m$,
$n$, $a$, $b$ be integers, and assume that the greatest common divisor of $m$
and $n$ is 1. Then there is an integer $x$ such that $x \equiv a$ (mod $m$)
and $x \equiv b$ (mod $n)$.**

Proposition 2.6 is the theorem describing the fact that, for two integers $i$
and $j$, $\gcd(i, j)$ generates the subgroup $i\Z + j\Z$.

Here's the proof from [A Mouri's solutions](https://github.com/AMouri/artin-algebra/blob/3083860baf553b472495fd01ef62489db9a261ee/Chapter%202%20-%20Groups/Section%209%20-%20Modular%20Arithmetic/solutions.tex#L66):

----------------------------------------------------------------------------

From Proposition 2.6, $1 = an + bm$. Then

$1 \equiv an + bm$ (mod $m$) $\rightarrow 1 \equiv an$ (mod $m$).

Since $\gcd(n, m) = 1$, then $n^{-1} \equiv a \mod m$. Similarly, $m^{-1}
\equiv b \mod n$.

----------------------------------------------------------------------------
My attempt:

We need to show that for any values $a,b$, we can always find an integer $x$
which exceeds the previous multiple of $m$ by $a$ and exceeds the previous
multiple of $n$ by $b$.

So we want to show that the intersection of $a + m\Z$ and $b + n\Z$ is
non-empty. I.e. we need to show that we can always find integers $r, s$
satisfying $a + rm = b +sn$. That's equivalent to $rm - sn = b - a$. We know
that $m\Z + n\Z = \gcd(m, n)\Z$, and thus since $\gcd(m, n) = 1$ we know that
$m\Z + n\Z$ is all of $\Z$. Therefore the integer $b - a$ must be reachable by
taking some number $b$ of steps of length $m$ and some number $-a$ of steps of
length $n$.

### E122 Homework 7

----------------------------------------------------------------------------


** 2.10.1 (E122 & 122) Let $G$ be the group of invertible real upper triangular
2 x 2 matrices. Determine whether or not the following conditions describe
normal subgroups $H$ of $G$. If they do, use the First Isomorphism Theorem to
identify the quotient group $G/H$. **

$G = \left\{ \mat{a}{b}
                 {0}{d} \right\}$

** (a) $a_{11} = 1$ **

$H = \left\{ \mat{1}{b}
                 {0}{d} \right\}$

This is closed, contains the identity and contains inverses, so it is a
subgroup. However, if we conjugate it with an arbitrary element
$\smat{e}{f}{g}{h}$ from $G$, the result is not in the subgroup, so it is not a
normal subgroup. Geometrically, I think this is because the matrix representing
the stretch-in-the-y-direction and shear-in-the-x-direction in the changed
basis does not also perform a stretch and shear in the corresponding directions
in the original basis.

\begin{align*}
&\mat{e}{f}
     {g}{h} \mat{1}{b}
                {0}{d} \mat{h}{-f}
                           {-g}{e} \frac{1}{eh - fg} \\
= &\mat{e}{f}
       {g}{h} \mat{h-bg}{-f + be}
                  {-dg }{de     } \frac{1}{eh - fg} \\
= &\mat{e(h-bg) - fdg}{e(-f + be) + fde}
       {g(h-bg) - hdg}{g(-f + be) + hde} \frac{1}{eh - fg}
\end{align*}

** (b) $a_{12} = 0$ **

$H = \left\{ \mat{a}{0}
                 {0}{d} \right\}$

This is closed, contains identity and inverses, hence is a subgroup. However
again, it is not closed under conjugation, so not normal. Geometrically, I
think this is because the matrix performing the stretch in orthogonal x- and
y-directions in the changed basis does not also perform a stretch in the
corresponding directions in the original basis.

\begin{align*}
&\mat{e}{f}
     {g}{h} \mat{a}{0}
                {0}{d} \mat{h}{-f}
                           {-g}{e} \frac{1}{eh - fg} \\
= &\mat{e}{f}
       {g}{h} \mat{ah}{-af}
                  {-dg}{de} \frac{1}{eh - fg} \\
= &\mat{eah - fdg}{-eaf + fde}
       {gah - hdg}{-gaf + hde} \frac{1}{eh - fg}
\end{align*}

** (c) $a_{11} = a_{22}$ **

$H = \left\{ \mat{a}{b}
                 {0}{a} \right\}$

Closed and contains identity and inverses, so a subgroup, but again not closed under conjugation.

\begin{align*}
&\mat{e}{f}
     {g}{h} \mat{a}{b}
                {0}{d} \mat{h}{-f}
                           {-g}{e} \frac{1}{eh - fg} \\
= &\mat{e}{f}
       {g}{h} \mat{ah - bg}{-af + be}
                  {-dg    }{de      } \frac{1}{eh - fg} \\
= &\mat{e(ah - bg) - fdg}{e(-af + be) + fde}
       {g(ah - bg) - hdg}{g(-af + be) + hde} \frac{1}{eh - fg}
\end{align*}


** (d) $a_{11} = a_{22} = 1$ **

$H = \left\{ \mat{1}{b}
                 {0}{1} \right\}$

Closed, contains identity and inverses. It performs a shear, with no
stretching. But again not closed under conjugation.

\begin{align*}
&\mat{e}{f}
     {g}{h} \mat{1}{b}
                {0}{1} \mat{h}{-f}
                           {-g}{e} \frac{1}{eh - fg} \\
= &\mat{e}{f}
       {g}{h} \mat{h - bg}{-f + be}
                  {-g    }{e      } \frac{1}{eh - fg} \\
= &\mat{e(h - bg) - fg}{e(-f + be) + fe}
       {g(h - bg) - hg}{g(-f + be) + he} \frac{1}{eh - fg}
\end{align*}


** 2.10.3 **

** 2.10.5 **

** 2.10.6 **

** 2.10.10 (122) **
