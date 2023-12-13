# Matrix Operations

Assume *A* , *B* , and *C* are matrices and $\alpha$ and $\beta$ are constants.

$$
A=\begin{bmatrix}
a & b & c \\
d & e & f  \\
\end{bmatrix}
$$

$$
A=\begin{bmatrix}
g & h & i \\
j & k & l  \\
\end{bmatrix}
$$

## Matrix Times Vector

Given a $m\times n$ matrix and a vector of size $n$

$$ \begin{bmatrix}
a_{11} & \cdots &  a_{1n} \\ 
\vdots & \ddots & \vdots \\ 
a_{m1} & \cdots & a_{mn}
\end{bmatrix} 

\times 

\begin{bmatrix} b_1 \\ \vdots \\  b_n \end{bmatrix}

= 

b_1 \begin{bmatrix}a_{11} \\ \vdots \\ a_{m1} \end{bmatrix} + \cdots  + b_n \begin{bmatrix}a_{1n} \\ \vdots \\ a_{mn} \end{bmatrix}
$$

## Matrix Times Matrix

**Dot Product Rule**

Given two matrices $A$ and $B$ of $m\times n$  and $n \times p$ sizes respectively (Where the number of rows in A is equal to the number of columns in B).

The $(i, j)$th entry of the resulting matrix is row $A_i$ $\cdot$ column $B_j$ (Row i of matrix A dotted with column j of matrix B).

## Determinants of a Matrix

**Definition 1**: If A is a 1x1 matrix, then $A = [a]$ , then $\det(A)=a$ 

**Definition 2**: If A is a 2x2 matrix, then $A = \begin{bmatrix}a & b \\ c & d\end{bmatrix}$ , then $\det(A)=ad-bc$ 

**Definition 3***: If A is an $n \times m$ matrix , then 
$$A = \begin{bmatrix}
a_{11} & \cdots &  a_{1n} \\ 
\vdots & \ddots & \vdots \\ 
a_{m1} & \cdots & a_{mn}
\end{bmatrix} 
\quad
\det(A)=
$$

*Determinants are recursive, you split a larger matrix into smaller ones to find the determinant for each and combine them accordingly.*

- To compute $\det(A)$, we can expand across any row/column
- It is better to simplify (using row ops) before computing $\det(A)$
> This is because the determinant of A does not change when row ops are applied

**There are 2 easy ways to tell if a the determinant of a matrix is 0**:
1. An entire *row* or *column* is = 0
2. 2 *rows* or *columns* are equal

# Invertible Matrices

> If A is a *square* matrix, a matrix B is the **inverse** of A if and only if
> $$AB=I\quad\land\quad BA=I$$

i.e. if matrix A and B multiply communitatively and the result is the *identity matrix*  A is the *inverse* of B and vice-versa.

# Elementary Matrices

- A matrix $A$ is *elementary* if the can be obtained from I using a *single* row operation. 
e. g.

If $E = R_1\rightarrow 3R_1+R_2=\begin{bmatrix}1 & 0 & 0 \\ 3 & 1 & 0 \\ 0 & 0 & 1\end{bmatrix}$

- Inverse of an elementary matrix is just the *inverse operation* that was used to obtain the elementary matrix.
- Can compute products/powers of elementary *matrices by repeating the row operation n times.*

e.g. 

$$
\begin{vmatrix}
1 & 0 \\
0 & 2
\end{vmatrix}^{10 }= 
\begin{vmatrix}
1 & 0 \\
0 & 2^{10}
\end{vmatrix}
$$

or 

$$
\begin{vmatrix}
1 & 0 \\
2 & 1
\end{vmatrix}^{10 }= 
\begin{vmatrix}
1 & 0 \\
2*10 & 1
\end{vmatrix}
$$

**Importance**:

Suppose A -> B takes one operation. If E = I correlated to this same row operation, then $B=EA$

*i.e. performing row operations are just performing matrix multiplications by an elementary matrix in disguise.*

This can be expanded express $B\rightarrow A$ in terms of elementary matrices. 

e.g.  Assuming we get B from A and $E_1$ is the first "row operation"

$$B=E_n ... E_2* E_1 * A \rightarrow A = (E_n*E_{n-1} ... E_2* E_1)^{-1}B$$

*We can also factor out invertible matrices in terms of elementary matrices.*

e.g. Assuming A is an *invertible* matrix and $E_1$ is the first "row operation"

$$E_n*E_{n-1} ... E_2 * E_1*A=I \rightarrow (E_n*E_{n-1} ... E_2 * E_1)^{-1}*I=A$$

# Eigenvalues

Eigenvalues are paired with *eigenvectors*

To find an *eigenvalue*  we use the formula: $$\det(A-\lambda I)=0$$

This comes from the equivalence $Ax=\lambda x=(\lambda I)x$ where $A$ is a square invertible matrix, and $x$ is our *eigenvector*

Removing the $x$ vector from our equation moving everything over to one side we get $A-(\lambda I)=0$. The only way this is true is if the determinant of the LHS is equal to 0. Therefore we get $\det(A-\lambda I)=0$

# Eigenvectors

Eigenvectors are paired with *eigenvalues*

To find an *eigenvalue*  we first have to find its corresponding [[#Eigenvalues|eigenvalue]] or $\lambda$. 

From there we sub in the value of the eigenvalue to the equation 

# Theorems

#determinants
*You cannot distribute determinants to matrices i.e $\det(A+B)\ne\det(A)+\det(B)$*

If A is a $n\times n$ matrix:
1. $\det(A^T)=\det(A)$
2. $\det(kA)=k^n\det(A)$

- - - 
#determinants 
If A, B are both $n\times n$:
> Prof. Hernandez calls it the "beautiful theorem"
- $\det(AB)=\det(A)\det(B)$

This provides a few things consequentially:
1. $\det(AB)=\det(A)\det(B)=\det(B)\det(A)=\det(BA)$
2. $\det(A_1 ... A_n)=\det(A_1) ... \det(A_n)$
3. If $A_1 ... A_n$ the previous formula becomes $\det(A^n)=\det(A)^n$

- - -
#determinants 
Suppose that A is $n\times n$ and also that A is *invertible*:
1. $\det(A)\ne0$
2. $\det(A^{-1})=\det(A)^{-1}=\frac{1}{\det(A)}$
2. $\det(A^{T})=\det(A)$

- - -
**If A is a square matrix, then the following statements are equivalent**
1. A is *invertible*
2. The only solution to $Ax=0$ is $x=0$
3. RREF of $A$ is $I$
4. A is a *product of elementary matrices*
5. The *determinant* of $A\ne0$
> $1\to2\to3 \to4\to5 \to1$

- - -
#determinants
If A is a square matrix and is invertible:
1. If a *multiple of a row is added to another row* $\det(A)=\det(A_1)$
2. If a *row is multiplied by a scalar $k$* then $\det(A)=k\det(A_1)$
3. If a *row is swapped with another* then $\det(A)=-1\det(A_1)$
4. If any *two rows or columns are identical* then $\det(A)=0$
5. If there exists a *row* or *column* of zeroes then $\det(A)=0$

- - -
#diagonalizeable
A square matrix $A$ is *diagonalizable* if we can factor $A$ as $A=PDP^{-1}$ where P=invertible and D=diagonal

Ideas:
1. Diagonal matrices are easy to deal with (compute det, eigenvalue, eigenvector, etc.)
2. If A is diagonalizable then A inherits those properties from D

- - - 
#diagonalizeable
A square matrix $A$ is diagonalizable if and only if we can build an invertible matrix P where columns are eigenvectors. In this case if $P=[x_1, x_2, ... x_n]$ which is also invertible


# Properties
> $\alpha$ and $\beta$ are both constants while $A$, $B$, and $C$ are all matrices.
- A + B = B + A
#associative-property
- (A + B) + C = A + (B + C) 
#communitaive-property
- $\alpha$(A + B) = $\alpha$A + $\alpha$B 
#distributive-property
- $\alpha + \beta$(A + B) = $\alpha$A + $\beta$B 
#distributive-property 
- ($\alpha\beta$)(A) = $\alpha$($\beta$A)
- $(A^T)^T=A$
- $(AB)^T=B^TA^T$ *order matters*
- $I$ is the identity matrix and has the same properties as the constant 1
- $IA=AI$ for all matrices
- *Inverted Matrices*
	- $B=A^{-1}$ exists exactly when $B=A^{-1}=\frac{1}{A}$ which should be $AB=BA=I$
	- $C=(AB)^{-1}=B^{-1}A^{-1}=I$ *order matters*
	- $(A^k)^{-1}=(A^{-1})^k$ *k can be a Transpose i.e.* $(A^T)^{-1}=(A^{-1})^T$

