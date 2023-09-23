# Overview

As the name suggest this focuses on [Linear Equations](https://en.wikipedia.org/wiki/Linear_equation) explicitly.

## *Systems* of *Linear Equations*

There are **3 operations** that can be performed on Linear Systems:
1. Interchanging two equations
2. Multiply one equations by a nonzero number
3. Add the multiple of one equation to another

**All** linear equations will fall under one of these three types of solutions:
1. No solution
2. One unique solution
3. $\infty$  solutions

> NOTE: This will not occur for *non-linear* equations

### Solving Systems of Linear Equations

Linear equations should only be simplified using invertible processes. This can be one of the three following operations:
- Changing the order of equations.
- Multiply an equation by an a *non-zero* constant.
- Add or subtract a multiple of an equation to another.

# Augmented Matrix Notation

**Elementary Operations**
1. Interchange two rows
2. Multiply one row by a scalar
3. Add a multiple of one row to another

> $\forall$  Examples 

**Interchange Two Rows**

$R_{i}\leftrightarrow R_{j}$

**Multiply a Row by a Scalar $C$**

$R_{i}\rightarrow C\cdot R_i$

e.g. $R_1\rightarrow R_1$

**Add a multiple of a Row to Another**

$R_{i}\rightarrow C\cdot R_j + R_i$

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

Using  row elimination operations, any system can be simplified in *RREF*. Moreover this reduced form is **unique**.

> This process is also called *gaussian elimination* #gaussian-elim

**Homogeneous Systems**

A homogeneous (linear) system is one in which every RHS is 0

e.g.

$$\begin{vmatrix} 
1 &2 &0 \\
2 &2 &0 \\
0 &6 &0 \\
\end{vmatrix}$$

> *Note*: Homogeneous system have many nice (special) properties!

Basic Properties of Homogeneous Systems:
- There is always one *trivial* solution; i.e. set all unknown vars = 0
- There is a Dichotomy of solutions, the *trivial* solution or $\infty$ many
- A  *Linear Combo* of solutions to a homogeneous system is also a solution. #linear-combo

# Applications

## Ancient Greeks

Any two distinct points determine a line.

Any 3 points that *do not lie on the same line*  determine a circle.

Any 5 points *provided that any 4 are not co-linear* determine a conic.
# Topics

## [[Vectors]]

## [[Math/Matrices]]