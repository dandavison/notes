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

Counts of two-locus genotypes (first number is SMN1 copy number, second number
is number of Alt alleles in SNP genotype).

\begin{align*}
\vec N =
&N_{10}, N_{11}, N_{12}, \\
&N_{20}, N_{21}, N_{22}, \\
&N_{30}, N_{31}, N_{32}, \\
&N_{40}, N_{41}, N_{42}, \\
\end{align*}


### Parameters of interest

Haplotype frequencies:

$$
\vec p = p_{00}, p_{01}, p_{10}, p_{11}, p_{20}, p_{21}
$$


### Model

Data is multinomial given two-locus genotype frequencies:

$$
\Pr(\vec N) \propto \prod F_{jk}^{N_{jk}}
$$

### EM Algorithm

#### E-step

For each individual, compute a probability distribution over its possible
haplotypes, using the current estimates of the haplotype
frequencies. Specifically:

1. For each individual $i$, and for each possible pair of haplotypes $g =
   \Big((j_1,k_1),(j_2,k_2)\Big)$, if the haplotype pair $g$ is consistent with
   $i$'s data then set
   $$
   q_{ig} \leftarrow \hat p_{j_1k_1} \hat p_{j_2k_2}
   $$
   (with factors of two when the haplotypes differ, to account for lack of unordering)
   If $g$ is inconsistent with $i$'s genotypes, then set $q_{ig} \leftarrow 0$.

2. For each individual $i$ and for each $g$, normalize these conditional
   probabilities by dividing by the sum:
   $$
   q_{ig} \leftarrow Pr\Big(G_i = g|X_i, \hat{ \vec p}\Big) = q_{ig} / \small{ \sum_{g'} } q_{ig'}
   $$
   Note that many of these entries will be equal to 1 because certain two-locus
   genotypes are consistent with only one haplotype pair. For example $10$
   is consistent only with $(1,0),(0,0)$.


#### M-step

Update the haplotype frequency parameters by weighting each individual
according to the probabilities computed in the E-step.

For each haplotype $(j,k)$:

$$
\hat p_{jk} \leftarrow \frac{ \sum_i q_{ig} }{2N}
$$
