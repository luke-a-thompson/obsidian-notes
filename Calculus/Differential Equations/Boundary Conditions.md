## Types of Boundary Conditions
Consider the heat equation
### Neumann
*Neumann* boundary conditions impose a spatial derivative of $0$ at both endpoints. 

**Example:**
For the heat equation, given $x$ is the length of a rod, the derivative would be $0$ at $x=0$ and $x=L$
$$
\frac{\partial T}{\partial x}(0,t) = \frac{\partial T}{\partial x}(L, t) \text{ for all } T>0
$$
### Periodic
*Periodic* boundary conditions impose that the solution (and sometimes its derivatives) is the same at the boundaries.

For a PDE on domain $x \in [a,b]$:
$$
u(a,t)=u(b,t),\quad \text{and optionally} \frac{\partial u}{\partial x}(a,t) = \frac{\partial u}{\partial x}(b,t)
$$**Example:**
Consider 1D [[Burger's Equation]] for modelling traffic flow on a circular track. If the cars start at $x=0$ and loop back at $x=L$, the speed of the cars $u(x,t)$ satisfies:
$$
u(0,t)=u(L,t)
$$