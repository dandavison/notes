Title: EM algorithm for haplotype frequency estimation
Slug: haplotype-frequency-em
Date: 2016-10-17

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


### Data

Counts of two-locus genotypes:

\begin{align*}
\vec N =
&N_{00}, N_{01}, N_{02}, \\
&N_{10}, N_{11}, N_{12}, \\
&N_{20}, N_{21}, N_{22}
\end{align*}


### Parameters of interest

Haplotype frequencies:

$$
\vec p = p_{00}, p_{01}, p_{10}, p_{11}
$$


### Model

Data is multinomial given two-locus genotype frequencies:

$$
\Pr(\vec N) \propto P_{jk}^{N_{jk}}
$$

### EM Algorithm

#### E-step

For each individual, compute a probability distribution over its possible
haplotypes, using the current estimates of the haplotype
frequencies. Specifically:

1. For each individual $i$, and for each possible pair of haplotypes $g =
   ((j_1,k_1),(j_2,k_2))$ that are consistent with $i$'s data:
   $$
   q_{ig} \leftarrow \hat p_{j_1k_1} \hat p_{j_2k_2}
   $$

   $$
   Pr\Big(G_i = g|X_i, \hat{ \vec p}\Big) \leftarrow \hat p_{j_1k_1} \hat p_{j_2k_2}
   $$
2. For each individual $i$, normalize this probability distribution by dividing by the sum.

#### M-step

Update the haplotype frequency parameters by weighting each individual
according to the probabilities computed in the E-step.

For each haplotype $(j,k)$:

$$
\hat p_{jk} \leftarrow \frac{ \sum_i Pr\Big(G_i=(j,k) | X_i, \hat p\Big) }{2N}
$$
