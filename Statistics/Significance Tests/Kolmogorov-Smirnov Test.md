The Kolmogorov-Smirnov (KS) test is a continuous analogue of the [[Chi-Square Test]]. It compares two distributions.

### Qualities
* Non-parametric - No assumption of normality
* Shape-only, no magnitude - Scales CDFs to between $0$ and $1$
* **Sensitive to high $n$ values - Exaggerates significance***
* Insensitive to tails as it focuses on largest deviation between CDFs
	* Resolved with the [[Anderson-Darling Test]]

### Key Values
* Test statistic - Max absolute difference between the CDFs of two distributions
* $H_{0}$ - Both distributions are identical
* Low $p$ indicates significant difference between distributions
* High $p$ indicates less difference between the distributions

### Scaling
1. Given a samples $X = {x_{1}, X_{2}, \dots , x_{n}}$, the empirical CDF is: $F_{n}(x) \frac{1}{n}\sum\limits_{i=1}^{n}I(x_{i}\leq x)$ 
	* $I(x_{i}\leq x)$ is an indicator function that is 1 if $x_{i} \leq x$, else $0$
	* $n$ is the number of datapoints
	* **This function counts how many values in $X$ are $\leq x$ and divides by the total sample size $n$
2. Scaling ensures $F_{n}(x) \in [0,1]$
	* Where $F_{n}(x)$ is the proportion of datapoints $\leq x$. Hence, they always range from $0$ to $1$
* The test works on the max absolute differences of the scaled CDFs