### Notation
The projection of a vector $v$ onto a vector $w$ is written as $proj_wv$.

### Vector Rejection - Projection for Generating Orthogonal Vectors
Subtracting the projection of $v$ onto $w$ produces a vector orthogonal to $v$.
1. Find the projection of $v$ onto $w$:
$$
proj_{w}v = \frac{v\cdot w}{w\cdot w}w
$$
2. Subtract this projection from $v$ to generate $u$, which is orthogonal to $w$:
$$u = v - proj_wv$$
3. $u$ is orthogonal to $w$
$$u \cdot w = 0$$This strategy is used extensively in the [[Gram-Schmidt]] method for [[QR Decomposition]]