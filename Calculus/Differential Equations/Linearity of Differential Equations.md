A differential equation (DE) is *linear* if it satisfies two properties:
1. Additivity: If $y_{1}, y_{2}$ are solutions, then $y_{1}+y_{2}$ is also a solution
2. Homogeneity: If $y$ is a solution and $c$ is a constant, $cy$ is also a solution

This yields the **superposition principle**.

## General Form of a Linear DE
A linear DE has the general form:
$$
a_{n}(x) \frac{d^ny}{dx^n}+a_{n-1}(x) \frac{d^{n-1}y}{dx^{n-1}}+\cdots + a_{1}(x) \frac{dy}{dx}+a_{0}(x)y=f(x)
$$Where:
* $a_{i}x$ are functions of the independent variables
* **No products or functions of $y$ or its derivatives appear**
	* $y'''+3yy'''+y=e^x$ would be non-linear as a function of $y$ appears before its third derivative
* $y$ and its derivatives are all to the first power