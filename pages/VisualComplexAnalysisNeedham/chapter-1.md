Title: Visual Complex Analysis - Needham - 1 Geometry and Compex Arithmetic
Slug: visual-complex-analysis-1
Date: 2016-11-12

<style type="text/css">
body {color: black;}
</style>

$$
\newcommand{\i}{\mathbf{i}}
\newcommand{\j}{\mathbf{j}}
\newcommand{\cvec}[2]{\begin{pmatrix}#1\\#2\end{pmatrix}}
\newcommand{\mat}[4]{\begin{bmatrix}#1 & #2\\#3 & #4\\ \end{bmatrix}}
\newcommand{\scvec}[2]{\tiny{\cvec{#1}{#2}}}
\newcommand{\smat}[4]{\tiny{\mat{#1}{#2}{#3}{#4}}}
\newcommand{\nth}{n^{\text{th}}}
$$

A complex number $z = x + iy$ is a point in the two-dimensional plane $\mathbb{C}$.

Addition is normal vector addition.

Multiplication is not obvious: $z_1z_2$ has angle equal to the sum of the two
angles, and length equal to the product of the two lengths.

In other words, multiplying by a complex number $z$ rotates by $z$'s angle, and
scales by $z$'s length.

For example: multiplying by $i$ is an anticlockwise rotation through 90°; $i^2 = -1$.

A complex number has infinitely many representations $(r, \theta)$ in polar
coordinates, with $\theta$ differing by multiples of $2\pi$.

**"Bombelli's wild thought"**: complex numbers are usually introduced by
considering the roots of a quadratic which does not intersect the
x-axis. However it is more compelling to consider solutions to a cubic
intersecting a line. In this case real solutions do exist, but they may require
complex arithmetic, and this arithmetic implies the addition and multiplication
laws.

**Obtaining symbolic from geometric rule**: Addition $z_1 + z_2$
describes a parallelogram. So multiplication $z_3(z_1 + z_2)$ describes a
rotated and shifted parallelogram. (...?)

**Obtaining geometric from symbolic rule**: Consider multiplying $z$ by $A =
4 + 3i = (5, tan^{-1}(\frac{3}{4}))$. We want to show that the algebraic result
is equivalent to rotating by $A$'s angle and scaling by $5$. Algebraically, $Az
= 4z + 3(iz)$. That describes a right-angle triangle with sides of length
$4|z|$ and $3|z|$. So the hypotenuse is length $5|z|$ as required, and since
the triangles are similar, their angles are the same and so we have rotated $z$
by $A$'s angle.

## Euler's formula

$e^{i\theta}$ is the point/vector on the unit circle at angle $\theta$:

$$
e^{i\theta} = cos \theta + i ~ sin \theta,
$$

and a generic complex number is $z = re^{i\theta}$. This makes the
multiplication law natural:

$$
(ae^{i\theta})(be^{i\phi}) = ab~e^{i(\theta + \phi)}.
$$

### Two justification's of Euler's formula

#### 1. Particle moving in $\mathbb{C}$

#### 2. Power series

