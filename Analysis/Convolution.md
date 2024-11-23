The *convolution* of two functions $f,g: \mathbb{R} \to \mathbb{R}$ is defined as:
$$
(f*g)(x) = \int_{-\infty}^{\infty} f(y)g(x-y) \, dy = \int_{-\infty}^{\infty} f(x-y)g(y) \, dy 
$$Where:
* $(f*g)(x)$ is the convolution operator
* The second equality holds due to [[Commutativity]]: $fg=gf$

Convolution measures how much two functions overlap as one slides over the other

Properties:
* Commutativity: $fg=gf$
* Associativity: $fg(h)=f(gh)$
* Distributivity over addition: $f*(g+h)=(fg)+(fh)$
* Associativity with scalars: $a(f*g) = af(g) = f(ag)$ for any scalar $A$
* Identity element: $f*\Delta =f$ where $\Delta$ is the [[Dirac Delta Function]]