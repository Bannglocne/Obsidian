# I. UNITS AND MEASUREMENT
## 1. The Scope and Scale of Physics
The **order of magnitude** of a number is the power of 10 that most closely approximates it. Thus, the order of magnitude refers to the scale (or size) of a value. An equivalent but quicker way to find the order of magnitude of a number is first to write it in scientific notation and then check to see whether the first factor is greater than or less than $\sqrt{10}$ ≈3

==Building Models==: 
- A **model** is a representation of something that is often too difficult (or impossible) to display directly
- A **theory** is a testable explanation for patterns in nature supported by scientific evidence and verified multiple times by various groups of researchers.
- A **law** uses concise language to describe a generalized pattern in nature supported by scientific evidence and repeated experiments.

## 2. Units and Standards
- A **physical quantity** either by specifying how it is measured or by stating how it is calculated from other measurements.

> [!NOTE] **Units** are standardized values. (SI units, English units, SAE units)
> In any system of units, the units for some physical quantities must be defined through a measurement process. These are called the **base quantities** for that system and their units are the **system’s base units**. All other physical quantities can then be expressed as algebraic combinations of the base quantities. Each of these physical quantities is then known as a **derived quantity** and each unit is called a **derived unit**.

| ISQ Base Quantity         | SI Base Unit  |
| ------------------------- | ------------- |
| Length                    | meter (m)     |
| Mass                      | kilogram (kg) |
| Time                      | second (s)    |
| Electrical current        | ampere (A)    |
| Thermodynamic temperature | kelvin (K)    |
| Amount of substance       | mole (mol)    |
| Luminous intensity       | candela (cd)  | 

| Prefix | Symbol | Meaning |
| ------ | ------ | ------- |
| yotta- | Y      | 10^24   |
| zetta- | Z      | 10^21   |
| exa-   | E      | 10^18   |
| peta-  | P      | 10^15   |
| tera-  | T      | 10^12   |
| giga-  | G      | 10^9    |
| mega-  | M      | 10^6    |
| kilo-  | k      | 10^3    |
| hecto- | h      | 10^2    |
| deka-  | da     | 10^1    |
| deci-  | d      | 10^-1   |
| centi- | c      | 10^-2   |
| milli- | m      | 10^-3   |
| micro- | µ      | 10^-6   |
| nano-  | n      | 10^-9   |
| pico-  | p      | 10^-12  |
| femto- | f      | 10^-15  |
| atto-  | a      | 10^-18  |
| zepto- | z      | 10^-21  |
| yocto- | y      | 10^-24  | 

The only rule when using metric prefixes is that you can not “double them up.”

## 3. Dimensional Analysis
The **dimension** of any physical quantity expresses its dependence on the base quantities as a product of symbols (or powers of symbols) representing the base quantities: $L^a M^b T^c I^d \Theta^e N^f J^g$

| Symbol for Dimension | Base Quantity       |     
| -------------------- | ------------------- | 
| L                    | Length              |     
| M                    | Mass                |     
| T                    | Time                |     
| I                    | Electric current    |     
| $\Theta$             | Temperature         |     
| N                    | Amount of substance |     
| J                    | Luminous intensity  |     

Equation must obey the following rules:
1. Every term in an expression must have the same dimensions
2. The arguments of any of the standard mathematical functions such as trigonometric functions (such as sine and cosine), logarithms, or exponential functions that appear in the equation must be dimension less. These functions require pure numbers as inputs and give pure numbers as outputs.


> [!NOTE] Physicists often use square brackets around the symbol for a physical quantity to represent the dimensions of that quantity
> [r] = L; [h] = L; [A] = $L^2$; [V] = $L^3$; [m] = M; [$\rho$] = M$L^3$

## 4. Significant Figures
**Accuracy** is how close a measurement is to the accepted reference value for that measurement.

The **precision** of measurements refers to how close the agreement is between repeated independent measurements (which are repeated under the same conditions).

The precision of a measuring system is related to the **uncertainty** in the measurements whereas the accuracy is related to the **discrepancy** from the accepted reference value.

=> $\text{Percent uncertainty} = \frac{\delta A}{A} \times 100\%$

1. **Method of adding percents**: The percent uncertainty in a quantity calculated by multiplication or division is the sum of the percent uncertainties in the items used to make the calculation
2. **Method of significant figures**: The last digit written down in a measurement is the first digit with some uncertainty.
3. When combining measurements with different degrees of precision, the number of significant digits in the final answer can be no greater than the number of significant digits in the least-precise measured value.
	- For multiplication and division, the result should have the same number of significant figures as the quantity with the least number of significant figures entering into the calculation.
	- For addition and subtraction, the answer can contain no more decimal places than the least-precise measurement

# II. VECTORS
## 1. Scalars and Vectors
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

### Algebra of Vectors in Two Dimensions
We follow the **parallelogram rule**.

## 2. Coordinate Systems and Components of a Vector
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

## 3. Algebra of Vectors
Vectors can be added together and multiplied by scalars.
1. $\alpha (\vec{A} + \vec{B}) = \alpha \vec{A} + \alpha \vec{B}$
2. $- \vec{A} = -\mathbf{A}_{x} \hat{\mathbf{i}}  -\mathbf{A}_{y} \hat{\mathbf{j}}  -\mathbf{A}_{z} \hat{\mathbf{k}}$
3. $\vec{A} = \vec{B}$ $\Leftrightarrow$ $$ \begin{cases} A_x = B_x \\ A_y = B_y \\ A_z = B_z \end{cases} $$
4. $$\begin{cases} F_{Rx} = \displaystyle\sum_{k=1}^{N} F_{kx} = F_{1x} + F_{2x} + \dots + F_{Nx} \\ F_{Ry} = \displaystyle\sum_{k=1}^{N} F_{ky} = F_{1y} + F_{2y} + \dots + F_{Ny} \\ F_{Rz} = \displaystyle\sum_{k=1}^{N} F_{kz} = F_{1z} + F_{2z} + \dots + F_{Nz} \end{cases} $$
5. $\hat{\mathbf{V}} = \frac{\vec{\mathbf{V}}}{V}$

## 4. Products of Vectors
- The **scalar product** $\vec{A}$.$\vec{B}$ of two vectors $\vec{A}$ and $\vec{B}$ is a number defined by the equation $$\vec{A}.\vec{B} = AB \cos{\varphi}$$ where $\varphi$ is the angle between the vectors. 
	- $\vec{A}.\vec{B} = \vec{B}.\vec{A}$
	- $\vec{A}.(\vec{B} + \vec{C}) = \vec{A}.\vec{B} + \vec{A}.\vec{C}$
	- $\vec{\mathbf{A}} \cdot \vec{\mathbf{B}} = A_x B_x + A_y B_y + A_z B_z$
	- $\cos \varphi = \frac{\vec{\mathbf{A}} \cdot \vec{\mathbf{B}}}{AB} = \frac{A_x B_x + A_y B_y + A_z B_z}{AB}$

- The **vector product** of two vector $\vec{A}$ and $\vec{B}$ is denoted by $\vec{A} \times \vec{B}$ and is often referred to as a **cross product**. The vector product is a vector that has its direction perpendicular to both vector $\vec{A}$ and $\vec{B}$. In other words, vector $\vec{A} \times \vec{B}$ is perpendicular to the plane that contains  $\vec{A}$ and $\vec{B}$. The magnitude of the vector product is defined as $$|\vec{A} \times \vec{B}| = AB \sin{\varphi}$$
where angle $\varphi$, between the two vectors, is measured from vector $\vec{A}$ (first vector in the product) to vector $\vec{B}$ (second vector in the product), and is between 0 and 180
	- $ $\vec{A}\times \vec{B} = -\vec{B}\times \vec{A}$$
	- $\vec{A}\times(\vec{B} + \vec{C}) = \vec{A}\times\vec{B} + \vec{A}\times\vec{C}$
	- $$ \begin{cases} \hat{\mathbf{i}} \times \hat{\mathbf{j}} = \hat{\mathbf{k}}  \\ \hat{\mathbf{j}} \times \hat{\mathbf{k}} = \hat{\mathbf{i}} \\ \hat{\mathbf{k}} \times \hat{\mathbf{i}} = \hat{\mathbf{j}} \end{cases} $$
	- $\vec{\mathbf{C}} = \vec{\mathbf{A}} \times \vec{\mathbf{B}} = (A_y B_z - A_z B_y) \hat{\mathbf{i}} + (A_z B_x - A_x B_z) \hat{\mathbf{j}} + (A_x B_y - A_y B_x) \hat{\mathbf{k}}$