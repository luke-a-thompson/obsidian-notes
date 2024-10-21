## Graph Isomorphism
Two graphs $G=(V_{G},E_{G})$ and $H = (G_{H}, E_{H})$ are isomorphic if there exists a bijection $f: V_{G} \rightarrow V_{H}$ such that:
$$
(u,v)\in E_{G} \equiv (f(u), f(v)) \in E_H
$$
This necessitates that the edges $e_{1}, e_{2}, \dots, e_{i} \in E_{G}$ under the isomorphism $f$ have the same adjacencies in $E_H$.

## Graph Properties
Graph properties are a class of graphs closed under isomorphism
* **Isomorphic graphs must always have the same properties**
	* A function assigning things to graphs, and the same things to isomorphic graphs
* E.g., the class of all graphs with $|V|=7$ is a property because isomorphic graphs have the same $|V|$

**Degree**
$\delta(G)$ is the minimum degree of a graph $G$.
