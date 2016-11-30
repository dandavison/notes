Title: Calculus
Slug: calculus
Date: 2016-11-28

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
\newcommand{\sumn}{\sum_{n=1}^{\infty}}
\newcommand{\limn}{\lim\limits_{n \to \infty}}
\newcommand{\limDt}{\lim\limits_{\Delta t \to 0}}
\newcommand{\dt}{\,\mathrm{d}t}
$$

Define $\int_a^b f(t) dt$ to be the area under the graph of $f(t)$ between
$t=a$ and $t=b$. This can be approximated as the sum of areas of rectangles,
where $t_i$ is the height of the $i\mathrm{th}$ rectangle.[ref]The rectangles
can be chosen so that their height is given by the value of $f(t)$ at either
their left or right endpoint, or in fact anywhere inbetween.[/ref]

$$
\int_a^b f(t) \dt = \limn \sum_{i=1}^n f(t_i) \Delta t
$$

----------------------------------------------------------------------------

### Fundamental Theorem of Calculus

Consider the case where $f(t)$ is the derivative of some function $F(t)$.

**Theorem:** The area under $F'(t)$ between $t=a$ and $t=b$ is $F(b) - F(a)$.

E.g. consider position $x(t)$ and its derivative velocity $x'(t)$. If someone
is stationary until time $t=a$, then moves at constant velocity $v$ until time
$t=b$, and then is stationary again, their total displacement is
$v(b-a)$. I.e. their displacement is equal to the rectangular area under the
graph of $x'(t)$.

** Attempted Proof:** (Is the following in the direction of a valid proof of part of FTC?)

\begin{align*}
\int_{a}^{b} F'(t) \dt
&= \limn \sum_{i=1}^n F'(t_i) \Delta t \\
&= \limDt \sum_{i=1}^{(b-a)/\Delta t} \frac{F(t_i + \Delta t) - F(t_i)}{\Delta t} \Delta t \\
&= \limDt \sum_{i=1}^{(b-a)/\Delta t} F(t_i + \Delta t) - F(t_i) \\
&= \limDt F(a + \Delta t) - F(a) + F(a + \Delta t + \Delta t) - F(a + \Delta t) + \ldots  + F(b - \Delta t + \Delta t) - F(b - \Delta t) \\
&= F(b) - F(a)
\end{align*}


#### Antiderivative
![ftc-position-velocity](/images/calculus/ftc-position-velocity.png)


----------------------------------------------------------------------------
