Title: Harvard E222 Algebra - Homework
Slug: harvard-e222
Date: 2016-12-08

$$
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
** 2.2.15 **
** 2.2.20(a) **


----------------------------------------------------------------------------

### E122 Homework 3

** 2.3.1 **

** 2.3.11 **

** 2.3.12 **

** 2.3.14 (122) **

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
**2.9.2**

----------------------------------------------------------------------------
**2.9.4**

----------------------------------------------------------------------------
**2.9.5**

----------------------------------------------------------------------------
**2.9.8**


** 2.10.1 (122) **

** 2.10.10 (122) **
