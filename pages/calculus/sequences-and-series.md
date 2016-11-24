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

### Typical questions about sequences (11.1)


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

### Series

If the series sums to a finite value then it is said to converge; if not, it diverges.

A series has an associated *sequence* of **partial sums**: $a_1, a_1 + a_2, a_1 + a_2 + a+3, ...$. I.e. the sequence $a_n = \sum_{i=1}^n a_i$. If the series sums to $s$ (converges) then $s$ is the limit of sequence of partial sums.

Say you only sum the first $n$ values of a series. The **remainder** $R_n$ is the difference between the true sum (of infinitely many values) and what you got from the first $n$ (the $\nth$ partial sum): $R_n = s - \sum_{i=1}^n$.



In general it is not easy to find the sum of a series, and so a lot of the material in the book focuses on methods for determining whether the series converges or not. However, it is easy to find the sum if the series is a *geometric series*:

#### Geometric series
Several questions require recognizing a geometric series. A geometric series is a series where each term differs by a constant multiplier:

$$
s = a + ar^1 + ar^2 + ar^3 + ... = \sumn ar^{n-1}
$$

Theorem: if $|r| < 1$ then the geometric series converges. Its value is $\frac{a}{1-r}$. For $|r| \geq 1$ it diverges.

### Typical questions about series

#### Find the values of x for which the series converges. Find the sum of the series for those values of x.

- 11.2.59
  $$
  \sum_{n=0}^{\infty} \frac{(x-2)^n}{3^n}
  $$
  We have to recognize that this is a geometric series. Rewrite it as
  $$
  \sum_{n=0}^{\infty} \Big(\frac{x-2}{3}\Big)^n
  $$
  and it's clear that it is a GS with $a=1$ and $r=\frac{x-2}{3}$. Therefore it converges if
  $$
  -1 < \frac{x-2}{3} < 1 \Leftrightarrow -1 < x < 5
  $$
  and when x is in that range, its sum is
  $$
  \frac{a}{1-r} = \frac{1}{1 - \frac{x-2}{3}} = \frac{3}{5-x}.
  $$

### Test for divergence of series
If the *sequence* does not converge to zero then the *series* (the sum of the infinite sequence) is divergent. That's fairly intuitive: if the sequence doesn't converge to zero then the series is going to be summing infinitely many non-zero terms and so will not converge.

So that means that most of the questions about series involve decreasing sequences that converge to zero, for example $a_n = \frac{1}{n}$, or $a_n = \frac{2}{(n-3)^2}$.

What's less intuitive is that even if the sequence *does* converge to zero, the series still might not converge. The famous example is $\sum_{n=1}^\infty \frac{1}{n} = \frac{1}{1} + \frac{1}{2} + \frac{1}{3} + ...$. Although the sequence converges to zero, its sum (the series) does not converge to a finite value. On the other hand, for $\sum_{n=1}^\infty \frac{1}{n^2} = \frac{1}{1} + \frac{1}{4} + \frac{1}{9} + ...$ the sequence converges to zero and the series does have a finite value. Those facts are not obvious, they require proof: both are infinite sequences of numbers that approach zero, it's just that one aproaches zero more rapidly and has a finite sum whereas the other approaches more slowly and fails to have a finite sum. We can prove it using the *integral test*.

### Integral test for convergence
Consider a series like $\sumn \frac{1}{n}$. The continuous function $f(x) = \frac{1}{x}$ passes through the discrete points of the sequence. The integral test says that we can use the area under the graph of the continuous function to assess whether the series converges. That's because we can visualize the series as summing together infinitely many rectangles of width 1, so the sum of the areas of the rectangle is related to the area under the graph.

**Integral test**: If $\int_1^\infty f(x) dx$ is convergent (has a finite value) then the series is convergent. And if the integral is divergent then the series is divergent.

For example
$$
\int_1^\infty \frac{1}{x^2} dx = \frac{-1}{x} \Big|_1^\infty = 1.
$$

so that shows that $\sumn \frac{1}{n^2}$ converges (to something, we don't know what). On the other hand

$$
\int_1^\infty \frac{1}{x} dx = \ln x \Big|_1^\infty = \lim_{x \to \infty} \ln x - 0
$$

which is divergent (not a finite value). So that shows that $\sumn \frac{1}{n}$ does not converge.

#### Remainder theorem for integral test
Because of the details of the location of the rectangle lines in the approximation, the size of the remainder lies between these two integrals:

$$
\int_{x=n+1}^\infty f(x) dx \leq R_n \leq \int_{x=n}^\infty f(x) dx
$$


### p-series

A p-series is a series like $\sumn \frac{1}{n^p}$.

Theorem: a p-series is convergent if $p>1$ and divergent if $p \leq 1$.

## Comparison tests

### Comparison to known-convergent series
Consider a series for which all terms are *positive*. If we can show that the terms of our series are always less than the corresponding terms of a known-convergent series, then our series is convergent. SImilarly if our terms are larger than those of a known-convergent series, then our series is divergent.

For example, we know that $\sumn\frac{1}{2^n}$ converges to zero (p-series with $p > 1$) but what about $\sumn\frac{1}{2^n + 1}$? It seems obvious that it converges to zero, but how do you prove it? The answer is that its terms are always smaller than the terms of $\sumn\frac{1}{2^n}$, therefore it also converges to zero.


### Limit comparison test
This involves looking at the limit of the *ratio* of the terms from two different series. Suppose you have a series $\sumn b_n$ which you know either converges or diverges, and you have a series $\sumn a_n$ which you don't know the behavior of. If you can show that their ratio has a finite limit:

$$
\limn \frac{a_n}{b_n} = c > 0
$$
then either *both converge* or *both diverge*. Seeing as you know how $b$ behaves, that tells you whether $a$ converges or not.


## Alternating series
The two theorems about alternating series are fairly obvious if we draw a picture of an alternating series.

## Alternating series test
The previous tests are all for series with positive terms only. Alternating series are often the result of a $(-1)^n$ factor, for example $\sumn (-1)^n \frac{1}{n}$. The *alternating series test* says: look at the absolute values; if they are decreasing (i.e. $a_{n+1} < a_n$), and if their limit is zero, then the series converges.


### Alternating series remainder theorem
The absolute size of the error is less than or equal to the size of the first neglected term. (Only for alternating series!)


## Absolute and conditional convergence

Sometimes a series with positive and negative terms might converge, but the absolute value version of the same series does *not* converge. This situation is called **conditional convergence**. An example is $\sumn (-1)^n \frac{1}{n}$. This converges (by alternating series test: the successive terms get smaller) but the absolute version doesn't converge (as discussed above).

If the absolute value version of an alternating series *does* converge, then this is called **absolute convergence**.

Theorem: if an alternating series is absolutely convergent, then the alternating version is convergent also.

In other words, there are two different categories of convergent alternating series: conditional (only the alternating version converges), and absolute (both versions converge).

## Ratio and tests

These can be used for alternating and non-alternating series.

### Ratio test
Write down the ratio of successive terms in the series $\frac{a_{n+1}}{a_n}$, take the absolute value and take the limit of that. So $\limn \Big|\frac{a_{n+1}}{a_n}\Big|$. There are 3 possible outcomes:

$$
\begin{cases}
0 < \text{limit} < 1&Convergent\\
\text{limit} = 1&Inconclusive\\
\text{limit} > 1 ~\text{or}~ \text{limit} = \infty&Divergent\\
\end{cases}
$$


### Root test
This is like the ratio test, but you use it if there are powers of $n$.

Evaluate the limit of the absolute value of the $\nth$ root of the $\nth$: $|\sqrt[n]{a_n}|$. The cases are the same as for the ratio test:


$$
\begin{cases}
0 < \text{root} < 1&Convergent\\
\text{root} = 1&Inconclusive\\
\text{root} > 1 ~\text{or}~ \text{root} = \infty&Divergent\\
\end{cases}
$$


## Strategy

See section 11.7 for overall strategy for testing series for convergence/divergence.


