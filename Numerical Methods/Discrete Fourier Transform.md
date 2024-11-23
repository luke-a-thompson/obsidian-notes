The *discrete Fourier transform* is a data-driven [[Fourier Series]] constructed from discrete data points. 

Given a vector of data $f = \{ f_{1}, f_{2},\dots f_{n} \}$ we can compute a vector of Fourier coefficients $\hat{f}= \{ \hat{f_{1}, \hat{f_{2}}},\dots \hat{f_{n}} \}$ via:
$$
\hat{f}_{k} = \sum_{j=0}^{n=1} = f_{j}e^{-i2\pi jk/n}
$$
Where:
* $\hat{f}_{k}$ is the $k$-th Fourier coefficient

I.e., the $k$-th Fourier coefficient is obtained as the sum