Leads to more stable weights, less likely to require large updates by significant changes to previous layers. 

May reduce condition number of the weight matrices?

## LayerNorm
Normalises each row of the weight matrix $X$ to be $X \sim N(0,1)$ via the **general formula for converting a gaussian to a 0 mean 1 variance form**:
$$
y = \frac{x=\mathbb{E}[x]}{\sqrt{Var[x]+\epsilon}} \times \gamma + \beta
$$ Where $\beta$ and $\gamma$ are learnable parameters.

## RMSNorm
Focus on rescaling (division by variance), not recentering.

Finds the RMS of each row of the weight matrix $X$, normalise according to:
$$
\bar{a} = \frac{a_i}{RMS(a)}g_i
$$
**Advantages:
* Computationally cheaper - Only RMS calc, no $\sigma$
* Empirically good
