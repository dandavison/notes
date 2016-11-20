Title: Sequences and series
Slug: sequences-series
Date: 2016-11-19

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
\newcommand{\ninfty}{n \rightarrow \infty}
$$

Notes on Stewart - Calculus ch. 11

-------------------------------------

## Definition of sequences and series

A **sequence** is an infinite sequence of numbers $a_1, a_2, a_3, ...$.

A **series** is the sum of a sequence: $s = a_1 + a_2 + a_3 + ... = \sum_{n=1}^\infty a_n$.

A sequence is often defined by giving the closed-form expression for the $\nth$ item, e.g. $a_n = \frac{1}{n}$. This refers to the sequence

$$\frac{1}{1}, \frac{1}{2}, \frac{1}{3}, ...$$

The corresponding series is

$$
\sumn \frac{1}{n} = \frac{1}{1} + \frac{1}{2} + \frac{1}{3} + ...
$$

A sequence may have a limit: $\lim_{n \rightarrow \infty} a_n$. If it does then the sequence *converges*. If not, it *diverges*.

**Divergence test for series:** The *series* (i.e. the infinite sum) can only have a finite value if the *sequence* converges to zero. But even then, it might not have a finite value. The famous example is $\sum_{n=1}^\infty \frac{1}{n} = \frac{1}{1} + \frac{1}{2} + \frac{1}{3} + ...$. Although the sequence converges to zero, its sum (the series) does not converge to a finite value. On the other hand, for $\sum_{n=1}^\infty \frac{1}{n^2} = \frac{1}{1} + \frac{1}{4} + \frac{1}{9} + ...$ the sequence converges to zero and the series does have a finite value. Those facts are not obvious, they require proof.

If the series sum is finite then the series *converges*; if not, it diverges.


## Typical questions about sequences (11.1)


#### Determine whether the sequence converges or diverges. If it converges, find the limit.

- **Easier** (11.1.24)
  $$
  a_n = \frac{n^3}{n^3 + 1}
  $$
  It's asking whether the sequence converges, so we want to try to compute the limit of the sequence as $n \rightarrow \infty$. If the limit exists then it converges. Rearrange so that all $n$s are on the bottom of fractions:
  $$
  a_n = \frac{1}{1 + \frac{1}{n^3}}
  $$
  So now
  $$
  \limn a_n = \frac{1}{1 + \limn\frac{1}{n^3}} = \frac{1}{1 + 0} = 1.
  $$

- **Easier** (11.1.26)
  $$
  a_n = \frac{n^3}{n + 1}
  $$
  With this one, we can't get the $n$s to appear only on the bottom of fractions:
  $$
  a_n = \frac{n^2}{1 + \frac{1}{n}}
  $$
  So
  $$
  \limn a_n = \frac{\limn n^2}{1 + \limn\frac{1}{n}} = \frac{\limn n^2}{1 + 0} = \limn n^2.
  $$
  But $n^2$ increases without bound as $\ninfty$. People write that as $\limn n^2 = \infty$. In any case, the limit does not exist and this sequence diverges.

- **Harder** (11.1.56)
  $$
  a_n = \frac{(-3)^n}{n!}
  $$
  The negative factor means that the terms of the sequence alternate between being negative and positive. Rewrite it as
  $$
  a_n = (-1)^n\frac{3}{1}\frac{3}{2}\frac{3}{3}\frac{3}{4}...\frac{3}{n-1}\frac{3}{n}
  $$
  Now we use two theorems in the book. The first ("Theorem 6") says that if $\limn |a_n|$ is zero, then so is $\limn a_n$. So that means we can see what happens while ignoring the -1 term. The second theorem is the "Squeeze Theorem": if we can show that the quantity we're studying lies between 0 and something else whose limit is zero, then we've proved that the limit of our quantity is 0. To do that we notice that all the terms from $\frac{3}{4}$ to $\frac{3}{n-1}$ are less than 1. Therefore
  $$
  0 < |a_n| < \frac{9}{2}\frac{3}{n} = \frac{27}{2n}
  $$
  But $\limn \frac{27}{2n} = 0$ so this (together with the Theorem 6 argument about the $(-1)^n$) proves that the sequence converges and that its limiting value is 0.
