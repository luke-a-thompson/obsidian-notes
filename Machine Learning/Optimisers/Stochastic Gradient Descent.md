## Assumptions
Let $f$ be our objective function:
- $f(x) = \frac{1}{n}\sum_{i=1}^n f_i(x)$ where $f_i$ is the loss for sample $i$
- $\nabla f(x) = \frac{1}{n}\sum_{i=1}^n \nabla f_i(x)$ is the full gradient
- $\nabla f_i(x)$ is the gradient of the loss for sample $i$
### Smoothness
- [[Lipschitz Continuity]]: $|\nabla f(x) - \nabla f(y)| \leq L|x-y|$
- Mean-squared [[Lipschitz Continuity|Lipschitz]] condition: $\mathbb{E}|\nabla f_{i}(x)|^{2} \leq M^{2}(1+|x-x^{*}|^{2})$
    - As we move away from the optimum $x^{*}$, the individual gradients increase in a quadratic manner
    - The growth is controlled by $M$
