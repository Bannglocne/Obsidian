 1. A **linear equation** in the variables $x_1,...,x_n$ is an equation that can be written in the form: $a_1x_1 +...+ a_nx_n = b$ where b and the **coefficients** $a_1,...,a_n$ are real or complex number
 
2. A **system of linear equations** (or a **linear system**) is a collection of one or more linear equations involving the same variables. A **solution** of the system is a list ($s_1,...,s_n$) of numbers that makes each equation a true statement when values $s_1,...,s_n$ are substituted for $x_1,...,x_n$
- The set of all possible solutions is called the **solution set** of the linear system. Two linear systems are called **equivalent** if they have the same solution set.

# Matrix
The essential information of a linear system can be recorded compactly in a rectangular array called a **matrix**. Given the system:

$$ \left\{ \begin{aligned} a_1x_1 + a_2x_2&=n_1 \\ b_1x_1 + b_2x_2&=n_2 \end{aligned} \right.$$
$$\begin{bmatrix}a_1&a_2\\b_1&b_2\end{bmatrix}$$ is called the **coefficient matrix** (or **matrix of coefficients**) of the system and the matrix $$\begin{bmatrix}a_1&a_2&n_1\\b_1&b_2&n_2\end{bmatrix}$$ is called the **augmented matrix** of the system
- The size of a matrix tell show many rows($m$) and columns($n$) it has: **$m \times n$ matrix**
- Elementary Row Operations:
	- (Replacement) Replace one row by the sum of itself and a multiple of another row.
	- (Interchange) Interchange two rows.
	- (Scaling) Multiply all entries in a row by a nonzero constant.
- If the augmented matrices of two linear systems are row equivalent, then the two systems have the same solution set.

## Echelon Forms
A rectangular matrix is in **echelon form** (or **row echelon form**) if it has the following three properties: 
1. All non zero rows are above any rows of all zeros. 
2. Each leading entry of a row is in a column to the right of the leading entry of the row above it. 
3. All entries in a column below a leading entry are zeros. 

If a matrix in echelon form satisfies the following additional conditions, then it is in **reduced echelon form**(or **reduced row echelon form**): 

4. The leading entry in each non zero rowis1. 
5. Each leading 1 is the only non zero entry in its column.

An **echelon matrix**(respectively, **reduced echelon matrix**)
$$
\begin{bmatrix}
0 & \blacksquare & * & * & * & * & * & * & * & * \\
0 & 0 & 0 & \blacksquare & * & * & * & * & * & * \\
0 & 0 & 0 & 0 & \blacksquare & * & * & * & * & * \\
0 & 0 & 0 & 0 & 0 & \blacksquare & * & * & * & * \\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & \blacksquare & * \end{bmatrix}
\quad
\begin{bmatrix}
0 & 1 & * & 0 & 0 & 0 & * & * & 0 & * \\
0 & 0 & 0 & 1 & 0 & 0 & * & * & 0 & * \\
0 & 0 & 0 & 0 & 1 & 0 & * & * & 0 & * \\
0 & 0 & 0 & 0 & 0 & 1 & * & * & 0 & * \\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 1 & * \end{bmatrix}
$$

> [!example] THEOREM I: Uniqueness of the Reduced Echelon Form 
> Each matrix is row equivalent to one and only one reduced echelon matrix

> [!info] DEFINITION
> A **pivot position** in a matrix A is a location in A that corresponds to a leading 1 in the reduced echelon form of A. A **pivot column** is a column of A that contains a pivot position

## The Row Reduction Algorithm
1. Begin with the left most non zero column. This is a pivot column. The pivot position is at the top.
2. Select a nonzero entry in the pivot column as a pivot. If necessary, interchange rows to move this entry into the pivot position
3. Use row replacement operations to create zeros in all positions below the pivot.
4. Cover (or ignore) the row containing the pivot position and cover all rows, if any, above it. Apply steps 1–3 to the submatrix that remains. Repeat the process until there are no more nonzero rows to modify
5. Beginning with the rightmost pivot and working upward and to the left, create zeros above each pivot. If a pivot is not 1, make it 1 by a scaling operation

## Solution of Linear Systems
$$ \left\{ \begin{aligned} a_1x_1 + a_3x_3&=n_1 \\ b_2x_2 + b_3x_3&=n_2 \\ 0 = 0 \end{aligned} \right.$$
$$ \left\{ \begin{aligned} x_1 = \frac{n_1 - a_3x_3}{a_1} \textbf{: basic variable} \\ x_2 = \frac{n_2 - b_3x_3}{b_1} \textbf{: basic variable} \\ x_3 \text{ is free} \textbf{: free variable} \end{aligned} \right.$$
The descriptions is **parametric description of solution sets** in which the free variables act as parameters. **Solving a system** amounts to finding a parametric description of the solution set or determining that the solution set is empty.

| Condition                                        | Outcome         | Geometric Intuition                                      |
| ------------------------------------------------ | --------------- | -------------------------------------------------------- |
| Row of $[0 \dots 0 \mid b]$ (where $b \neq 0$)** | Inconsistent    | Parallel lines/planes that never meet.                   |
| Consistent + No Free Variables                   | Unique Solution | Lines/planes intersecting at a single point.             |
| Consistent + At Least One Free Variable          | Infinitely Many | Intersecting along a line or a higher-dimensional plane. |

---
# [[Vector]] Equations
