Differentiable functions $\subset$ Continuous functions.

# Continuity
For a function $f(x)$ to be continuous, the following properties must hold for every point $a$:
* $f(a)$ is defined
* $\lim_{x \rightarrow a}f(x)$ exists
	* Requires that $\lim_{x \rightarrow a^{-}}f(x) = \lim_{x \rightarrow a^{+}}f(x)$![[Pasted image 20241027002135.png]]
* $\lim_{x\rightarrow a}f(x) = f(a)$

# Differentiability
Describes how smooth a function is - essentially, how many times the derivative can be taken.

For a function to be differentiable, the following properties must hold for every point $a$:
*  $f'(a)$ exists
	* The derivative is defined as $f'(a) = \lim_{h \rightarrow 0} \frac{f(a+h)-f(a)}{h}$
	* The left and right limits must agree
		* $\lim_{h \rightarrow 0^{+}} \frac{f(a+h)-f(a)}{h} = \lim_{h \rightarrow 0^{+}} \frac{|h|-|0|}{h} = \lim_{h \rightarrow 0^{-}} \frac{h}{h} = 1$
		* $\lim_{h \rightarrow 0^{-}} \frac{f(a+h)-f(a)}{h} = \lim_{h \rightarrow 0^{-}} \frac{|h|-|0|}{h} = \lim_{h \rightarrow 0^{-}} \frac{-h}{h} = -1$
			* $-h$ because the absolute value function does a sign-flip

## Levels of Differentiability
* $C^{0}$ - Continuous functions
	* $f(x) = |x|$ is not differentiable as 
* $C^{1, \dots, n}$ - Order $n$ differentiable
* $C^{\infty}$ - Smooth (infinitely differentiable) functions
	* Still infinitely differentiable if the derivatives become 0
	* $f(x) = x^{3}$
	* $f(x) = e^{x}$
