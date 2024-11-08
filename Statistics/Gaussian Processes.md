## Kernels
**What they do in GPs**
1. Relating inputs & outputs
	* The [[Kernels|kernel]] function $k(x,x')$ measures the similarity between two inputs $x, x'$.
	* If $x, x'$ are "close" according to the kernel, their corresponding outputs $f(x), f(x')$ should be strongly correlated. Hence, their $y$ values should be similar.
2. Smoothness, correlation 
	* **Small input changes result in small output changes**
	* If kernel inputs are close, the covariance between their outputs is large, so their outputs are likely to be close in value
	* This property ensures the functions are smooth - Differentiable to some order
	* Some kernels enforce weaker smoothness - Matern kernels
3. Incorporates prior knowledge
	* If one thinks the underlying function is periodic, they can select a periodic kernel
	* Specifying the kernel allows specifying how much the function is expected to change between nearby points
4. Interpolation, extrapolation
	* Allows interpolation between observed points
	* Kernel assess how much new datapoint depends on nearby observed points
	* If the kernel implies distant points are uncorrelated, the GP does not make confident predictions far from the observed data*
5. Uncertainty
	* Points farther apart in kernel distance are predicted with greater uncertainty. It's assumed the function values at these points are less correlated.
