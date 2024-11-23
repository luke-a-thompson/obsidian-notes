The *heat equation* models how heat diffuses throughout a material. It is defined as:
$$
\frac{\partial T}{\partial t} = k \nabla^{2}T = k\frac{\partial^{2}T}{\partial x^{2}}
$$Where:
* $T$ is temperature
* $t$ is time
* $x$ is the position in the material
* $k$ is the thermal conductivity
* $\nabla^{2}$ is the [[Div, Grad, Curl#^d58b6a|Laplacian]] which always operates on spatial coordinates.

Hence,
$\frac{\delta T}{\delta t}$ is the change in temperature at a fixed position $x$. We are looking at one spot.
$\frac{\delta^{2}T}{\delta x^{2}}$ is the spatial temperature gradient over position at a fixed time $t$. We are looking at a spot and how its affected by its neighbours.

If $\frac{\partial^{2}T}{\partial x^{2}} >0$: The temperature profile curves upward, so this point is colder than it's neighbours.

## As Gradient Flow
We can interpret the heat equation as a [[Gradient Flow]] with respect to the [[Dirichlet Energy]] functional:
$$
\mathcal{E}^\text{Dir}(T) = \frac{1}{2} \int_{\Omega} \left| \frac{\partial T}{\partial x} \right|^2 dx
$$This measures the "smoothness" of the temperature distribution $T$ across the spatial domain $\Omega$. Smoother distributions correspond to lower energy values,

The gradient of $\mathcal{E}^\text{Dir}(T)$ w.r.t. $T$ via the [[Euler-Lagrange]] equation is:
$$
\frac{\partial \mathcal{E}^\text{Dir}}{\partial t}=-\frac{\partial^2T}{\partial x^2}
$$This is the direction in which $T$ should change to most effectively decrease $\mathcal{E}^\text{Dir}$.

So the heat equation therefore becomes:
$$
\frac{\partial T}{\partial t} = -k \frac{\partial \mathcal{E}^\text{Dir}}{\partial T} = k \frac{\partial^2 T}{\partial x^2}
$$As the second derivative is embedded in the functional's gradient.

## Physical Interpretation
* Heat flows from high $T$ > low $T$, with flow $\propto \Delta T$ between the points
* Each point tends toward the mean of its neighbours
* Derivatives 
	* $\frac{\partial T}{\partial x}$: Spatial temperature gradient 
		* $> 0$: Temperature increases rightward
		* $< 0$: Temperature decreases rightward 
	* $\frac{\partial^2 T}{\partial x^2}$: Temperature curvature 
		* $> 0$: Point colder than neighbor average (may increase)
		* $< 0$: Point hotter than neighbor average (may decrease)
	* ![[Pasted image 20241030011427.png]]