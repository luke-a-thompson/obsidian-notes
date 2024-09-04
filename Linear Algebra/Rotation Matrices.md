An [[Orthogonality#Matrix Case|orthogonal]] matrix which rotates points in the plane by $\theta$ radians.

Consider a vector where $\cos$ determines the $x$ coordinate and $\sin$ determines the $y$ coordinate.
$$\begin{bmatrix}1\\0\end{bmatrix} = \begin{bmatrix}\cos(\theta)\\\sin(\theta)\end{bmatrix} $$
We can rotate this counter-clockwise to form:
$$\begin{bmatrix}0\\1\end{bmatrix} \begin{bmatrix}-\sin(\theta)\\\cos(\theta)\end{bmatrix}$$
Now,$\cos$ becomes $-\sin$ as the $x$ coordinate is now negative and $\sin$ becomes $\cos$ as it now determines the $y$ coordinate.

This gives a final rotation matrix:
$$A = \begin{bmatrix}\cos(\theta) & -\sin(\theta) \\ 
\sin(\theta) & \cos(\theta)\end{bmatrix}$$
Trick:
Start with cosine and sin, differentiate to find the second column.

Rotation is a unitary transformation, so $det(A) = 1$.

![[Pasted image 20240714221338.png]]