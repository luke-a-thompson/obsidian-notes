Equation:
$$
F(X) = \frac{1}{\sqrt{4 \pi t}} \int^{\infty}_{\infty} f(y)e^{\frac{(x-y)^2}{4t}}dy
$$
Where:
* $e^{\frac{(x-y)^2}{4t}}$ is a Gaussian function centred at $y=x$ with width $t$
	* Ensures $f(y)$ is smoothed around $x$
* $t$ controls smoothing
	* as $t \rightarrow 0$ , the kernel becomes more localised approximating the Dirac delta function
* $\frac{1}{\sqrt{4\pi t}}$ ensures the Gaussian function integrates to $1$ over all $y$
	* Makes it a proper convolution with $f(y)$
	* Preserves magnitude - Ensures the energy of the signal is unchanged during transformation
	* Smoothing - Like blurring, normalising the kernel to integrate to $1$ ensures it just redistributes the signals locally, rather than amplifying or diminishing
* $\int^{\infty}_{\infty}$ is infinite as its a convolution between $f(y)$ and the Gaussian kernel