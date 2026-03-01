# Scalars and Vectors
**Scalar** is a synonym of “number.” Time, mass, distance, length, volume, temperature, and energy are examples of scalar quantities.

Physical quantities specified completely by giving a number of units (magnitude) and a direction are called **vector** quantities.

**Displacement** is a general term used to describe a change in position. The length of the arrow represents the magnitude $\mathbf{D}$ of vector $\vec{\mathbf{D}}$: $\mathbf{D} \equiv |\vec{\mathbf{D}}|$

### Algebra of Vectors in One Dimension
- $\vec{A}$ is **parallel** to $\vec{B}$ if they have same direction and |$\vec{A}$| = |$\vec{B}$|
- $\vec{A}$ is **antiparallel** to $\vec{B}$ if they have different directions and |$\vec{A}$| = |$\vec{B}$|
- $\vec{B}$ = $\alpha$.$\vec{A}$ => B =|α|A.
- $\vec{\mathbf{D}}_{AD} = \vec{\mathbf{D}}_{AC} + \vec{\mathbf{D}}_{CD}$: **Resulant** vector
- **Commutative**: $\vec{A} + \vec{B} = \vec{B} + \vec{A}$
- **Associative**: $(\vec{A} + \vec{B}) + \vec{C} = \vec{A} + (\vec{B} + \vec{C})$
- **Distributive**: $\alpha_1 \vec{A} + \alpha_2 \vec{A} = (\alpha_1 + \alpha_2) \vec{A}$
- A **unit vector** ($\hat{u}$) has a magnitude of one and does not have any physical unit so that |$\hat{u}$| = u = 1
---
## Algebra of Vectors in Two Dimensions
We follow the **parallelogram rule**.

# Coordinate Systems and Components of a Vector
$\vec{A} = \vec{\mathbf{A}}_{x} + \vec{\mathbf{A}}_{y}$ with 
$\begin{cases}  \vec{\mathbf{A}}_x = A_x \times \hat{\mathbf{i}} \\  \vec{\mathbf{A}}_y = A_y \times \hat{\mathbf{j}} \end{cases}$ => **The component form** of a vector: $\vec{\mathbf{A}} = A_x \times \hat{\mathbf{i}} + A_y \times \hat{\mathbf{j}}$

If we know the coordinates b($\mathbf{x}_{b}$, $\mathbf{y}_{b}$) of the origin point of a vector (where b stands for “beginning”) and the coordinates e($\mathbf{x}_{e}$, $\mathbf{y}_{e}$) of the end point of a vector: $$
\begin{cases} 
A_x = x_e - x_b \\ 
A_y = y_e - y_b 
\end{cases}
$$ => $A^2 = A_x^2 + A_y^2 \Leftrightarrow A = \sqrt{A_x^2 + A_y^2}$ and the **direction angle** $\mathbf{θ}_{A}$: $\tan \theta = \frac{A_y}{A_x}$
$$ \begin{cases} A_x = A \cos \theta_A \\ A_y = A \sin \theta_A \end{cases} $$

**Polar Coordinates**: $$ \begin{cases} x = r \cos \varphi \\ y = r \sin \varphi \end{cases}$$
---
# Algebra of Vectors
Vectors can be added together and multiplied by scalars.
1. $\alpha (\vec{A} + \vec{B}) = \alpha \vec{A} + \alpha \vec{B}$
2. $- \vec{A} = -\mathbf{A}_{x} \hat{\mathbf{i}}  -\mathbf{A}_{y} \hat{\mathbf{j}}  -\mathbf{A}_{z} \hat{\mathbf{k}}$
3. $\vec{A} = \vec{B}$ $\Leftrightarrow$ $$ \begin{cases} A_x = B_x \\ A_y = B_y \\ A_z = B_z \end{cases} $$
4. $$\begin{cases} F_{Rx} = \displaystyle\sum_{k=1}^{N} F_{kx} = F_{1x} + F_{2x} + \dots + F_{Nx} \\ F_{Ry} = \displaystyle\sum_{k=1}^{N} F_{ky} = F_{1y} + F_{2y} + \dots + F_{Ny} \\ F_{Rz} = \displaystyle\sum_{k=1}^{N} F_{kz} = F_{1z} + F_{2z} + \dots + F_{Nz} \end{cases} $$
5. $\hat{\mathbf{V}} = \frac{\vec{\mathbf{V}}}{V}$
---
# Products of Vectors
- The **scalar product** $\vec{A}$.$\vec{B}$ of two vectors $\vec{A}$ and $\vec{B}$ is a number defined by the equation $$\vec{A}.\vec{B} = AB \cos{\varphi}$$ where $\varphi$ is the angle between the vectors. 
	- $\vec{A}.\vec{B} = \vec{B}.\vec{A}$
	- $\vec{A}.(\vec{B} + \vec{C}) = \vec{A}.\vec{B} + \vec{A}.\vec{C}$
	- $\vec{\mathbf{A}} \cdot \vec{\mathbf{B}} = A_x B_x + A_y B_y + A_z B_z$
	- $\cos \varphi = \frac{\vec{\mathbf{A}} \cdot \vec{\mathbf{B}}}{AB} = \frac{A_x B_x + A_y B_y + A_z B_z}{AB}$

- The **vector product** of two vector $\vec{A}$ and $\vec{B}$ is denoted by $\vec{A} \times \vec{B}$ and is often referred to as a **cross product**. The vector product is a vector that has its direction perpendicular to both vector $\vec{A}$ and $\vec{B}$. In other words, vector $\vec{A} \times \vec{B}$ is perpendicular to the plane that contains  $\vec{A}$ and $\vec{B}$. The magnitude of the vector product is defined as $$|\vec{A} \times \vec{B}| = AB \sin{\varphi}$$
where angle $\varphi$, between the two vectors, is measured from vector $\vec{A}$ (first vector in the product) to vector $\vec{B}$ (second vector in the product), and is between 0 and 180
	- $\vec{A}\times \vec{B} = -\vec{B}\times \vec{A}$$
	- $\vec{A}\times(\vec{B} + \vec{C}) = \vec{A}\times\vec{B} + \vec{A}\times\vec{C}$
	- $$ \begin{cases} \hat{\mathbf{i}} \times \hat{\mathbf{j}} = \hat{\mathbf{k}}  \\ \hat{\mathbf{j}} \times \hat{\mathbf{k}} = \hat{\mathbf{i}} \\ \hat{\mathbf{k}} \times \hat{\mathbf{i}} = \hat{\mathbf{j}} \end{cases} $$
	- $\vec{\mathbf{C}} = \vec{\mathbf{A}} \times \vec{\mathbf{B}} = (A_y B_z - A_z B_y) \hat{\mathbf{i}} + (A_z B_x - A_x B_z) \hat{\mathbf{j}} + (A_x B_y - A_y B_x) \hat{\mathbf{k}}$
