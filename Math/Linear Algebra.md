# Overview

As the name suggest this focuses on [Linear Equations](https://en.wikipedia.org/wiki/Linear_equation) explicitly.

## *Systems* of *Linear Equations*

**All** linear equations will fall under one of these three types of solutions:
1. No Solution
2. One Unique Solution
3. $\infty$ many solutions

> NOTE: This will not occur for *non-linear* equations

### Solving Systems of Linear Equations

Linear equations should only be simplified using invertible processes. This can be one of the three following operations:
- Changing the order of equations.
- Multiply an equation by an a *non-zero* constant.
- Add or subtract a multiple of an equation to another.

# Notation

$$a=
\begin{vmatrix}
a & b & c \\
i & j & k \\
x & y & z \\
\end{vmatrix}$$
> $\forall$  Examples 

**Multiply a Row by a Scalar $C$**

$R_{i}\rightarrow C\cdot R_i$

e.g. $R_1\rightarrow R_1$

# Definitions:

**Augmented Matrices**:

![[Pasted image 20230823113640.png]]

**Gaussian Elimination**:
#gaussian-elim

1. Put 1 in the top left col.
2. Use this leading 1 to eliminate all other value in that column
3. Repeat this process for each remaining row.

**Echelon Form** :
#echelon-form

A matrix is in echelon form if:
- The bottom row consists of only 0
- The left most non-zero entry of each row is to the right of the leading entry from the row above.

**Reduced Row Echelon Form (RREF)**:

A matrix is reduced if:
- It is in *echelon form*. #echelon-form
- A leading $1$ is the only non-zero value in the row.

# Theorems

Using  row elimination operations, any system can be simplified in *RREF*. Moreover this reduced form is **unique**.
> This process is also called *gaussian elimination* #gaussian-elim

# Topics

## [[Vectors]]