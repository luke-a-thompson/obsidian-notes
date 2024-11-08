A σ-algebra $\mathcal{A}$ over a set $X$ is a collection of subsets of $X$:
$$
\mathcal{A} \subset \mathcal{P}(X)
$$Where $\mathcal{P}$ is a [[Power Set]] of $X$.
### Measurable Sets
$A \in \mathcal{A}$ is a *measurable set* of $\mathcal{A}$.

## Properties of $\sigma$-Algebras
1. Contains itself and the empty set: $\emptyset, X \in \mathcal{A}$
2. Closed under complement: $A \in \mathcal{A} \implies A^{C} \coloneqq X \setminus A \in \mathcal{A}$  
	* I.e., If $A$ is a measurable set in $\mathcal{A}$, everything outside $A$, denoted $A^{C}$ also belongs to $\mathcal{A}$ and is measurable.
	* ![[Pasted image 20241102193649.png]]
3. Closed under uncountable unions: $\bigcup\limits_{i=1}^{\infty}A_{i}\in \mathcal{A}$
	* I.e., For any countable collection of sets $A_{1}, A_{2},\dots \in \mathcal{A}$, their union must also be in $\mathcal{A}$. The sum of all countable sets is the total volume.
	* ![[Pasted image 20241102195637.png]]

**Example:**
* Smallest $\sigma$-algebra: $\mathcal{A} = \{\emptyset, X\}$
* Largest $\sigma$-algebra: $\mathcal{A} = \mathcal{P}(X)$
	* Usually, we cannot measure all possible subsets as in the largest case here.
	* **Best to have a number of measurable sets as close as possible to $\mathcal{A} = \mathcal{P}(X)$
