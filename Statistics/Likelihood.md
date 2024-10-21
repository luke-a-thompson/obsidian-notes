## Why log the likelihood?
* Likelihood is the sum of probabilities > can become small when many variables involved - Less likely with log
* Log product of probabilities becomes sum, easier to compute: $\log (\prod\limits_{i=1}^{n} p(x_i|\theta)) = \sum\limits_{i=1}^{n} \log p(x_{i}|\theta)$ 
	* Given independent observations $x_{1}, x_{2}, \dots x_{n}$ , the likelihood is a product: $p(x_{1}, x_{2}\dots x_{n}|\theta) = \prod\limits_{i=1}^{n} p(x_{i}|\theta)$
	* But using log likelihood simplifies this product into a sum: $\log p(x_{1}, x_{2}, \dots, x_{n}|\theta) = \sum\limits_{i=1}^{n} \log p (x_{i}|\theta ))$
* Improves convergence of optimization by increasing convexity > easier to find maximum likelihood estimates (MLE)
* Relates directly to bits of information