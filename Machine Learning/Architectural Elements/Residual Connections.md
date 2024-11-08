## Ungated Residuals
Traditional form from ResNet, adds the input of a block directly to it's output to prevent vanishing gradients:
$$
f(x) + x
$$

## Gated Residuals
Enables a learnable function to control how much of the block's original input is added to the output.
$$
y = g(x) \cdot f(x) + (1-g(x)) \cdot x
$$
Where $g(x)$ is a function who's data $x$ is first transformed by a learnable weight matrix $W$ and bias $b$ like:
$$
g(x) = \frac{1}{1+e^{-z}} (Wx+b)
$$With just a linear layer and no function $g$, the transformation on $x$ would be inbounded and could lead to instability or non-smoothness.
