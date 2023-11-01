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

### Theorems

*You cannot distribute determinants to matrices i.e $\det(A+B)\ne\det(A)+\det(B)$*

If A is a $n\times n$ matrix:
1. $\det(A^T)=\det(A)$
2. $\det(kA)=k^n\det(A)$
- - - 
If A, B are both $n\times n$:
> Prof. Hernandez calls it the "beautiful theorem"
- $\det(AB)=\det(A)\det(B)$

This provides a few things consequentially:
1. $\det(AB)=\det(A)\det(B)=\det(B)\det(A)=\det(BA)$
2. $\det(A_1 ... A_n)=\det(A_1) ... \det(A_n)$
3. If $A_1 ... A_n$ the previous formula becomes $\det(A^n)=\det(A)^n$
- - -
Suppose that A is $n\times n$ and also that A is *invertible*:
1. $\det(A)\ne=0$
2. $\det(A^{-1})=\det(A)^{-1}=\frac{1}{\det(A)}$

## Elementary Matrices

- A matrix $A$ is *elementary* if the can be obtained from I using a *single* row operation. 
- Inverse of an elementary matrix is just the *inverse operation* that was used to obtain the elementary matrix.

e.g. 

If $E = R_1\leftarrow$
- Can compute products/powers of elementary matrices by repeating the row operation *n* times.

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
20 & 1
\end{vmatrix}
$$

**Importance**:

Suppose A -> B takes one operation. If E = I correlated to this same row operation, then $B=EA$

*i.e. performing row operations are just performing matrix multiplications by an elementary matrix in disguise.*

## Properties
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
- *Inverted Matrices*
	- $I$ is the identity matrix and has the same properties as the constant 1
	- $IA=AI$ for all matrices
	- $B=A^{-1}$ exists exactly when $B=A^{-1}=\frac{1}{A}$ which should be $AB=BA=I$
	- $C=(AB)^{-1}=B^{-1}A^{-1}=I$ *order matters*
	- $(A^k)^{-1}=(A^{-1})^k$ *k can be a Transpose i.e.* $(A^T)^{-1}=(A^{-1})^T$

## Theorems

**If A is a square matrix, then the following statements are equivalent**
1. A is *invertible*
2. The only solution to $Ax=0$ is $x=0$
3. RREF of $A$ is $I$
4. A is a *product of elementary matrices*
5. The *determinant* of $A\ne0$
>$1 -> 2 -> 3 -> 4 -> 5 \to 1