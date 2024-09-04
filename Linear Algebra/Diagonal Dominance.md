### Weak Diagonal Dominance
A matrix $A$ is weakly diagonally dominant if the absolute value of the diagonal entry of all rows is $\geq$ the sum of the absolute values of all other (off-diagonal) entries of those rows or column.

A weakly row diagonally dominant matrix satisfies:
$$|a_{jj}| \geq \sum_{j\neq{i}}\limits{|a_{ij}|}\ \forall i$$
Whilst a weakly column dominant matrix satisfies:
$$|a_{jj}| \geq \sum_{j\neq{i}}\limits{|a_{ji}|}\ \forall i$$

### Strict Diagonal Dominance
$A$ is strictly row diagonally dominant if the following holds:
$$|a_{jj}| > \sum_{j\neq{i}}\limits{|a_{ij}|}\ \forall i$$
Or $A$ is strictly column diagonally dominant if:
$$|a_{jj}| \geq \sum_{j\neq{i}}\limits{|a_{ji}|}\ \forall i$$

### Proof via [[Gershgorin Circle Theorem]]
1. If all diagonal entries $a_{ii}$ of matrix $A$ are positive, the centres of all [[Gershgorin Circle Theorem#Gershgorin Discs|Gershgorin discs]] are positive
2. The radius of each Gershgorin disc *must* be less than the value of the diagonal entry itself:
3. 
