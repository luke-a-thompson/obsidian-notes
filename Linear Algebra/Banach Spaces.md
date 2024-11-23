A *Banach space* is a complete normed [[Vector Space]]. A space $V$ is a Banach space if the following holds:
1. It is a vector space: Defines $+$ and scalar multiplication
2. It has a norm $\|\cdot\|$ satisfying
	1. $\|x\| \geq 0$
	2. $\|x\|=0 \Longleftrightarrow x=0$: Positive definite
	3. $\|ax\|=\|a\|\|x\|$: Homogenous
	4. $\|x+y\| \leq \|x\| + \|y\|$: Triangle inequality
3. Complete: Every Cauchy sequence converges in the space
	* I.e., $\|x_{n}-x_{m}\| \to 0$ as $n,m \to \infty$

## Separability
A Banach space $X$ is *separable* if it contains a [[Countability|countable]], [[dense]] subset. Formally, a subset $S \subseteq X$ is dense if:
$$
\forall x\in X, \epsilon>0, \exists s\in S:\|x-s\|<\epsilon
$$Intuitively, any point in the Banach space $X$ can be described as being arbitrarily close to some point in $S$. I.e., it is topologically manageable.

Examples:
* $\mathbb{R}^n$ with $\ell_{2}$ norm
	* $\mathbb{R}^0$, but is pathological
* $\ell^p$ spaces of $p$-summable sequences
	* Let $\ell^{p}\coloneqq \ell^{p}(\mathbb{N}, \mathbb{F})$ where $\mathbb{F} \in {\mathbb{R}, \mathbb{C}}, p \in [1,\infty)$
	* All sequences $(X_{n})_{n\in \mathbb{N}}$ in $\mathbb{F}$ such that $\sum_{n=1}^\infty |x_{n}|^p < \infty$ converges
	* Then, $\|\cdot\|_{p}:\ell^p \to [0, \infty)\ \text{with}\ \|x|_{p}:=\left(\sum_{n=1}^\infty|x_{n}|^p\right)^\frac{1}{p}\ \text{is a norm!}$
* $L^p$ spaces of $p$-integrable functions
* $C[a,b]$, continuous functions with $\sup$ norm