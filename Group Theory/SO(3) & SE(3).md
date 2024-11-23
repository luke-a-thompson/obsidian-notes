## SO(3)
The *special orthogonal group in 3D* or $SO(3)$ is the group of all $3\times 3$ matrices with $\det(1)$ representing 3D rotations:
$$
SO(3)=\{R\in \mathbb{R}^{3\times3}|R^TR=I, \det(R)=1\}
$$
Properties:
* Only rotational: $3$ DoF (roll, pitch yaw)
* Associated [[Lie Algebra]]: $\mathfrak{so}(3)$
* 

## SE(3)
The *special Euclidean group in 3D* is the group of all **rigid body** transformations in 3D:
$$
SE(3)=\{(R,t)|R\in SO(3), t\in \mathbb{R}^3\}
$$It is represented as a homogenous [[Transformation Matrix]]:
$$
\begin{bmatrix}
R&T\\0&1
\end{bmatrix},R\in SO(3),t\in \mathbb{R}^3
$$

Properties:
* Combines $SO(3)$ rotations and $\mathbb{R}^3$ rotations: $6$ DoF
* Associated [[Lie Algebra]]: $\mathfrak{se}(3)$