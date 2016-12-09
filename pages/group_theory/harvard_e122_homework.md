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
$$


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

**2.6.4 Give an example showing that left cosets and right cosets of $GL_2(\R)$
  in $GL_2(\C)$ are not always equal.**

We don't even need to consider matrices outside $\GL_2(\R)$. Let A =
$\smat{1}{0}
      {0}{0}$ and let $H = \GLR{2}$.

Geometrically, this matrix projects points in 2D onto the x-axis.

The left coset of $\GLR{2}$ containing $A$ is the set of matrices of the form

$$
\smat{1}{0}
     {0}{0} \smat{a}{b}
                 {c}{d} = \smat{a}{b}
                               {0}{0}
$$

where $a,b,c,d \in \R$. Geometrically, this composition first sends the basis
vectors to new locations with x-coordinates $a$ and $b$, and then projects onto
the x axis.

The right coset of $\GLR{2}$ containing $A$ is the set of matrices of the form

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
