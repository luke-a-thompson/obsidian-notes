## Pointwise Convolution
A *pointwise* or $1 \times 1$ convolution is an [[Affine Transformation]] applied independently to each input "pixel":
$$
y_{i,j,k} = \sum_{c=1}^{C_{in}} w_{k,c} \cdot x_{i,j,c} + b_k
$$
Where:
* $x_{i,j,c}$ is the input spatial position $i,j$ in channel $c$
* $Y_{i,j,c}$ is the output spatial position $i,j$ in channel $c$
* $w_{k,c}$ is the weight connecting input channel $c$ to output channel $k$
* $b_{k}$ is the bias for channel $k$
* $C_{in}$ is the number of input channels
* $k \in \{1,\dots, C_{out}\}$ where $C_{out}$ is the number of output channels

An equivalent matrix representation would be:
$$
\mathbf{y}_{ij} = \mathbf{Wx}_{ij} + b
$$Where:
* $\mathbf{x}_{ij} \in \mathbb{R}^{C_{in}}$
* $\mathbf{W} \in \mathbb{R}^{C_{out}\times C_{in}}$
* $\mathbf{b \in \mathbb{R}^{C_{out}}}$
* $\mathbf{y}_{ij} \in \mathbb{R}^{C_{out}}$

**They are useful to reduce or expand dimensionality across channels and add non-linearities.**