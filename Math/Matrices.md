# Matrix Operations

Assume *A* , *B* , and *C* are matrices and $\alpha$ and $\beta$ are constants.

$$
A=\begin{vmatrix}
a & b & c \\
d & e & f  \\
\end{vmatrix}
$$

$$
A=\begin{vmatrix}
g & h & i \\
j & k & l  \\
\end{vmatrix}
$$

## Matrix Times Vector

Given a $m\times n$ matrix and a vector of size $n$

$$ \begin{bmatrix}
a_{11} & \cdots &  a_{1n} \\ 
\vdots & \ddots & \vdots \\ 
a_{m1} & \cdots & a_{mn}
\end{batrix} 

\times 

\begin{vmatrix} b_1 \\ \vdots \\  b_n \end{vmatrix}

= 

b_1 \begin{vmatrix}a_{11} \\ \vdots \\ a_{m1} \end{vmatrix} + \cdots  + b_n \begin{vmatrix}a_{1n} \\ \vdots \\ a_{mn} \end{vmatrix}
$$

## Properties

A + B = B + A #associative-property
(A + B) + C = A + (B + C) #communitaive-property
$\alpha$(A + B) = $\alpha$A + $\alpha$B #distributive-property
$\alpha + \beta$(A + B) = $\alpha$A + $\beta$B #distributive-property 
($\alpha\beta$)(A) = $\alpha$($\beta$A)
$(A^T)^T=A$

