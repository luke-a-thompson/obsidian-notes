The *Chi-squared distribution* is a distribution of the sum of squares of $k$ independent standard normal random variables. It is a special case of the [[Gamma Distribution]] and a univariate case of the [[Wishart Distribution]].

If $Z_{1}, Z_{2},\dots,Z_{k}$ are i.id. random variables s.t. $Z_{i}\sim(0,1)$, the random variable $X$ follows a Chi-square distribution with $k$ degrees of freedom:
$$
X = \sum\limits_{i=1}^{k}Z_{i}^{2}
$$We can denote this as:
$$
X \sim \mathcal{X}^{2}(k)
$$

Properties:
* $\mu =k$
* $\sigma =2k$
* If $X \sim \mathcal{X}^{2}(k_{1})$ and $Y \sim \mathcal{X}^{2}(k_{1})$ are independent, then $x+Y \sim \mathcal{X}^{2}(k_{1}+k_{2})$
* As $k \to \infty$, $\mathcal{X}^{2}\approx \mathcal{N}(k,2k)$ 
