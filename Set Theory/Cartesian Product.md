The *cartesian product* of the sets $A$ and $B$, denoted $A \times B$ is the set of **all** ordered pairs:
$$
A \times B = \{(a,b)|a \in A, b \in B\}
$$
**Examples:**
- $\{1,2\} \times \{3,4\} = {(1,3), (1,4), (2,3), (2,4)}$
- $\mathbb{R} \times \mathbb{R} = \mathbb{R}^2$ (the plane)
- If $A=\{a,b,c\}$, $|A\times A|$ = 9 
- Multiplication can be viewed as a function $f: \mathbb{R} \times \mathbb{R} \rightarrow \mathbb{R}$ where $f(x,y) = xy$
    - The input is a *pair* of numbers (from the Cartesian product)
    - The output is their product

A subset $G_{f} \subseteq A\times B$ is a *function* if:
$$
\forall x \in A: \exists y\in B:(x,y) \in G_{f}
$$This represents a mapping $f: A \rightarrow B$, or equivalently $f(x) =y$ for $(x,y) \in G_f$. $G_{f}$ is the *graph* of $f$, whilst $A$ is the domain of $f$ and $B$ is the codomain.
## Functions as Relations
A _function_ $f: A \rightarrow B$ can be defined as a special subset $G_f \subseteq A \times B$ (called its _graph_) where:

1. Existence (total): $\forall x \in A: \exists y \in B: (x,y) \in G_f$
2. Uniqueness: If $(x,y_1) \in G_f$ and $(x,y_2) \in G_f$ then $y_1 = y_2$

The graph $G_f$ is the set of all input-output pairs of a function. It represents the mapping $f: A \rightarrow B$ where:
$$f(x)=y⟺(x,y)∈Gf​ \text{ for } x∈A,y∈B$$

with $A$ as the _domain_ and $B$ as the _codomain_.

**Example**:
- For $f(x) = x^2$ on $\mathbb{R}$, the graph is all points $(x,x^2)$
- When we "plot a function", we are literally drawing its graph
- Every point on the curve is an ordered pair $(x,f(x))$ in the Cartesian product
