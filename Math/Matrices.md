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

## Properties

A + B = B + A #associative-property
(A + B) + C = A + (B + C) #communitaive-property
$\alpha$(A + B) = $\alpha$A + $\alpha$B #distributive-property
$\alpha + \beta$(A + B) = $\alpha$A + $\beta$B #distributive-property 
($\alpha\beta$)(A) = $\alpha$($\beta$A)
$(A^T)^T=A$

