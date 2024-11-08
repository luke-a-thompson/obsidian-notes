## Power Rule
$$
\frac{d}{dx}x^{n}=nx^{n-1}
$$
## Exponential Rule
$$
\frac{d}{dx}e^{x}=e^{x}
$$
## Trigonometric Rules
$$
\begin{align}
\frac{d}{dx}&=\sin(x) = \cos(x)\\
\frac{d}{dx}&=\cos(x) = -\sin(x)
\end{align}
$$
## Sum Rule
Take the derivative of each function separately and add the results. If $f(x) = g(x)+h(x)$, then $f'(x) = g'(x)+h'(x)$.
$$
\frac{d}{dx}(f(x)+g(x)) = \frac{df}{dx}+\frac{dg}{dx}
$$
## Product Rule
Take the derivative of the first function multiplied by the second, and add it to the derivative of the second function multiplied by the first. If $f(x) = g(x)h(x)$, then $f'(x)=g'(x)h(x)+g(x)h'(x)$.
$$
\frac{d}{dx}(f(x)g(x))=\frac{df}{dx}g(x)+f(x)\frac{dg}{dx}
$$
## Chain Rule
Take the derivative of the outside function, multiply it by the derivative of the inside function.
$$
\frac{d}{dx}(f(g(x)))=\frac{df}{dg}\frac{dg}{dx}
$$Example:
$$
\begin{align}
&f=sin(x), g=2(x)\\
&\frac{d}{dx}(sin(2x)) \\
=\ &\frac{d}{dg}(sin(g))\cdot \frac{d}{dx}(2x)\\
=\ &\cos(g)\cdot2 \quad \text{$\leftarrow$ Becomes 2 via power rule} \\
=\ &cos(2x)\cdot2
\end{align}
$$
## Reciprocity
$$
\frac{dx}{df} = \frac{1}{\frac{df}{dx}}
$$
