# Overview
The Quaternions $\mathbb{H}$ are a group of numbers with the following properties:
- $\mathbf{i}^2 = \mathbf{j}^2 = \mathbf{k}^2 = \mathbf{ijk} = -1$
- Have the form $a + b\mathbf{i} + c\mathbf{j} + d\mathbf{k}$

Each basis $\text{i}$, $\text{j}$, and $\text{k}$ of the quaternion represents a "unit plane" of each of the respective axes with area $1$.  These bases can be known as *basis [[Bivector]]*.  The basis bivectors must be mutually orthogonal.  

Bivectors are *not* vectors.  They are instead planes defined by two vectors.  This means that *having a component in one of the bivector "axes" corresponds to a signed area on the plane defined by the bivector*.  There is no kind of position relative to the bivector plane.  Only a signed area.

A bivector represents the minimum information required in any given dimension to store both a plane and a magnitude.

Quaternions show up when dealing with rotations because *rotations happen **in** a plane, **not** around an axis*.

# Derivation
Assume you have some pair of vectors: 
$$\mathbf{a} = \left ( x_a, y_a, z_a \right ) \quad \mathbf{b} = \left ( x_b, y_b, z_b \right )$$  
and we want to know the product $\mathbf{ab}$. We can represent each vector algebraically via:
$$
\begin{align}
\mathbf{a} &= x_a\mathbf{x} + y_a\mathbf{y} + z_a\mathbf{z} \\
\mathbf{b} &= x_b\mathbf{x} + y_b\mathbf{y} + z_a\mathbf{z}
\end{align}
$$
where $\mathbf{xyz}$ are basis vectors in three dimensions.

The product of the two vectors is thus:
$$
\begin{align}
\mathbf{ab} &= (x_a\mathbf{x} + y_a\mathbf{y} + z_a\mathbf{z})(x_b\mathbf{x} + y_b\mathbf{y} + z_b\mathbf{z}) \\
&= x_ax_b\mathbf{xx} + x_ay_b\mathbf{xy} + x_az_b\mathbf{xz} \\
&\quad + y_ax_b\mathbf{yx} + y_ay_b\mathbf{yy} + y_az_b\mathbf{yz} \\
&\quad + z_ax_b\mathbf{zx} + z_ay_b\mathbf{zy} + z_az_b\mathbf{zz}
\end{align}
$$

However, the meaning of $\mathbf{xz}$, $\mathbf{xx}$, etc. is not yet clear.  In order to understand this expression, first recall that the length of any vector is given as:
$$
||\mathbf{v}|| = \sqrt{\sum{v_i^2}}
$$
which implies that:
$$
||\mathbf{v}||^2 = \sum{v_i^2}
$$
Also note the axiom that for any vector $\mathbf{v}$:
$$
\mathbf{v}^2 = ||\mathbf{v}||^2
$$
Since for any unit vector, $\mathbf{x}$, $\mathbf{y}$, or $\mathbf{z}$ the length is $1$:
$$
\begin{align}
\mathbf{x}^2 = ||\mathbf{x}||^2 = 1 \\
\mathbf{y}^2 = ||\mathbf{y}||^2 = 1 \\
\mathbf{z}^2 = ||\mathbf{z}||^2 = 1
\end{align}
$$
we can determine that our product $\mathbf{ab}$ reduces to:
$$
\begin{align}
\mathbf{ab} = &\quad x_ax_b + y_ay_b + z_az_b + \\
&\quad x_ay_b\mathbf{xy} + x_az_b\mathbf{xz} + \\
&\quad y_ax_b\mathbf{yx} + y_az_b\mathbf{yz} + \\
&\quad z_ax_b\mathbf{zx} + z_ay_b\mathbf{zy}
\end{align}
$$
To determine the meaning of $\mathbf{xy}$, $\mathbf{zx}$, etc. first we must consider that the length of the sum of two basis vectors is $\sqrt{2}$:
$$
||\mathbf{x} + \mathbf{y}|| = \sqrt{1^2 + 1^2} = \sqrt{2}
$$
again using the axiom above:
$$
\begin{align}
(\mathbf{x} + \mathbf{y})^2 &= (\sqrt{2})^2 \\
\mathbf{xx} + \mathbf{xy} + \mathbf{yx} + \mathbf{yy} &= 2 \\
1 + \mathbf{xy} + \mathbf{yx} + 1 &= 2 \\
\mathbf{xy} + \mathbf{yx} &= 0 \\
\mathbf{xy} &= -\mathbf{yx}
\end{align}
$$
This means that for any pair of orthonormal basis vectors, we can swap and negate the product.  Doing so transforms our product $\mathbf{ab}$ into:
$$
\begin{align}
\mathbf{ab} &= x_ax_b + y_ay_b + z_az_b + \\
&\quad x_ay_b\mathbf{xy} - y_ax_b\mathbf{xy} + \\
&\quad x_az_b\mathbf{xz} - z_ax_b\mathbf{xz} + \\
&\quad y_az_b\mathbf{yz} - z_ay_b\mathbf{yz} \\
&= x_ax_b + y_ay_b + z_az_b + \\
&\quad (x_ay_b - y_ax_b)\mathbf{xy} + \\
&\quad (x_az_b - z_ax_b)\mathbf{xz} + \\
&\quad (y_az_b - z_ay_b)\mathbf{yz}
\end{align}
$$
We have now simplified our product to contain only one of each $\mathbf{xy}$ term.  Now let us consider what squaring one of these terms produces:
$$
(\mathbf{xy})^2 = \mathbf{xyxy} = -\mathbf{xxyy} = -1 \cdot 1 = -1
$$
Since $(\mathbf{xy})^2 = -1$, it follows that:
$$
(\mathbf{xy})^2 = \text{i}^2
$$
and 
$$
(\mathbf{xy})^2 = (\mathbf{zx})^2 = (\mathbf{yz})^2 = -1
$$
and finally
$$
\begin{align}
(\mathbf{xy})(\mathbf{zx})(\mathbf{yz}) &= \mathbf{xyzxyz} \\
&= -\mathbf{xyzxzy} \\
&= \mathbf{xyzzxy} \\
&= \mathbf{xyxy} \\
&= -1
\end{align}
$$

giving us the identity:
$$
(\mathbf{xy})^2 = (\mathbf{zx})^2 = (\mathbf{yz})^2 = (\mathbf{xy})(\mathbf{zx})(\mathbf{yz}) = -1
$$
which is more commonly known as:
$$
\text{i}^2 = \text{j}^2 = \text{k}^2 = \text{ijk} = -1
$$
which satisfies our definition of a Quaternion as our product can be written as:
$$
\begin{align}
\mathbf{ab} &= (x_ax_b + y_ay_b + z_az_b) + \\
&\quad(x_ay_b - y_ax_b)\text{i} + \\
&\quad(x_az_b - z_ax_b)\text{j} + \\
&\quad(y_az_b - z_ay_b)\text{k}
\end{align}
$$

The product can also be rewritten as the sum of the dot and wedge products:
$$
\mathbf{ab} = \mathbf{a} \cdot \mathbf{b} + \mathbf{a} \land \mathbf{b}
$$

where the wedge product is defined as:
$$
\begin{align}
\mathbf{a} \land \mathbf{b} &= \mathbf{yz}(y_az_b - z_ay_b) + \\
&\quad \mathbf{zx}(z_ax_b - x_az_b) + \\
&\quad \mathbf{xy}(x_ay_b - y_ax_b)
\end{align}
$$
