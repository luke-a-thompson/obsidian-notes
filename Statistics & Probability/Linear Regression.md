Linear regression aims to find the coefficients $\beta$ so that $\hat{y} = X \beta$ are as close as possible to the actual target values $y$. This is done by minimising the squared residuals:

$$
\begin{align}
\text{Conventional notation: } &J(\beta)=\sum\limits_{i=1}^{n}(y_{i}-X_{i}\beta)^2\\
\text{Matrix notation: } &J(\beta) = \|y-X\beta\|^{2}=(y-X\beta)^{T}(y-X\beta) \\
\end{align}
$$

## L1 and L2 Norm

## *Normal Equation* - Analytic Solution
Requires $X^{T}X$ to be non-singular, and hence the system to be neither under- or over-determined.

Process:
* Expand the cost function to the quadratic form: $J(B) = y^{T}y-2\beta^{t}X^{T}y+\beta^{T}X^{T}X\beta$
	* It's "quadratic" because $\beta$ is squared as it appears twice on the right side
* Take the derivative of the cost function: $\frac{\partial J(\beta)}{\partial \beta} = -2X^{T}y+2X^{T}X\beta$
* Set the derivative to $0$: $-2X^{T}y+2X^{T}X\beta = 0$
* Solve for $\beta$: $X^{T}X\beta=X^{T}y$
* Rearranging: $\beta = (X^{T}X)^{-1}X^{T}y$

## Under- and Over-determination

Equations are the number of datapoints - $X$
Weights and biases are the unknowns - $\beta$

Overdetermined
* More equations (data points) than unknowns (features)
* More common in practice
* No exact solution, 
* $n>p$, hence tall skinny matrix
	* Consider $X$ with 20 data points (rows) and 3 samples (columns)
	* The coefficient vector $\beta$ then has 3 rows, 1 column as its transposed to enable matmul
	* If $X$ is of full rank, there is no exact solution as there are insufficient entries in $\beta$ to produce as many linearly independent values to output to the $y$ vector

Underdetermined
* More Fewer data points than features
* Infinite solutions - Overfitting risk
* $n<p$, hence short fat matrix
	* There are more unknowns in $\beta$, so some are free variables, there are infinite solutions