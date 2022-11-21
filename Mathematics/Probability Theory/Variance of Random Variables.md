**Sunday Nov 20, 2022** #probability

---

### Requires

1. [[Expectation of Random Variables]]

---

### Definition

The variance of a random variable can be thought of as a measure of spread, where we sum the distances of each observation from the mean squared:
$$
\begin{align}
\sigma^{2}_{X} = var(X) &= E[(X - E(X))^2] \\ \\
& = \sum_{x}(x-E(x))^{2}P_{X}(x)
\end{align}
$$
We notice that $(x - E(X))^{2}$ is a random variable itself, and it itself is non-negative. It is only 0 when $X = c$ (a constant). We also notice that by linearity of expectation:
$$
\begin{align}
\sigma^{2}_{X} &= E[(X - E(x))^{2}] \\
&= E[X^{2} -2XE(X) + E^{2}(X)] \\
&= E(X^{2}) + E(-2E(X)X) + E^{2}(X) \\
&= E(X^{2}) - 2E(X)E(X) + E^{2}(X) \\
&= E(X^{2}) - E^{2}(X)
\end{align}
$$
