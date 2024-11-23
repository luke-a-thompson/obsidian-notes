The *Fourier transform* is a generalisation of the [[Fourier Series]] to non-period functions by representing any function $f(x)$ as the superposition of complex exponentials. In angular frequency this is written as:
$$
\mathcal{F}(\omega) = \mathcal{F}\{ f(x) \}=\int_{\infty}^\infty f(x)e^{-i\omega x}dx
$$
Where:
* $\mathcal{F}(\Omega)$ is the Fourier transform of $f(x)$
* $\omega$ is the angular frequency (radians per unit $x$)
* $e^{-i\omega x}$ is the complex exponential basis function
* The integral is a continuous sum over all space/time

The *inverse Fourier transform* recovers the original function $f(x)$:
$$
f(x) = \mathcal{F}^{-1}\{ F(\omega) \}= \frac{1}{2\pi} \int_{-\infty}^{\infty} F(\omega)e^{i\omega x} \, d\omega
$$Where:
* $\frac{1}{2\pi}$ is a scaling factor. Needed as $\frac{1}{2\pi}$ is absorbed into the $\omega$ in the forward Fourier transform
* The integral is a continuous sum over the contributions of all frequencies
## Existence Conditions
* Absolutely integrable: $\int_{-\infty}^{\infty} |f(x)| \, dx <0$ or [[Square-Integrable Functions|square integrable]]

## Fourier Domain
A function $f(x)$ can be analysed in two domains:
* Spatial/time: Values of $f(x)$ at each point $x$
* Fourier/frequency: Values of $F(\omega)$ representing the amplitude of each frequency $\Omega$

Properties:
* Multiplication
	* $\mathcal{F}(f*g)=\mathcal{F}(f)\cdot \mathcal{F}(g)$, where $\cdot$ denotes pointwise multiplication
	* **Multiplication in the Fourier domain is equivalent to convolution in the spatial domain**
	* **Example**: Blurring an image by convolving with a Gaussian kernel $g(x)=e^{-x^2}$ is equivalent to multiplying by $G(\omega)=\sqrt{\pi}e^{-\omega^2/4}$ in Fourier space
* Differentiation
	* $\mathcal{F} \frac{d}{dx}f(x) = i \Omega F(\omega)$
	* Each derivative multiples by $i \omega$ in the Fourier domain
	* **Example**: For $f(x)=\sin(ax)$, $\frac{d}{dx}f(x)=a\cos(ax)$. In Fourier space, this is multiplication by $i\omega$ at $\omega=\pm a$
* Translation
	* $\mathcal{F}f(x-a)=e^{-i \omega a}F(\omega)$
	* Spatial shifts become phase shifts in the Fourier domain
	* **Example**: Shifting a Gaussian $e^{-x^2}$ by 2 units right to $e^{-(x-2)^2}$ corresponds to multiplying its Fourier transform by $e^{-2i\omega}$