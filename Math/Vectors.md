# Special Vectors

The *zero-vector* has **no magnitude** and **no direction**. in $\mathbb{R}^2$ and $\mathbb{R}^3$

A *unit vector* is a vector with [[#magnitude]] of 1 or $$||\vec{v}||=1$$

## Standard Basis Vectors

In $\mathbb{R}^2$:  $\textbf{i}=\langle1,0\rangle$ and $\textbf{j}=\langle0,1\rangle$

In $\mathbb{R}^3$:  $\textbf{i}=\langle1,0,0\rangle$ and $\textbf{j}=\langle0,1,0\rangle$ and $\textbf{j}=\langle0,0,1\rangle$

# Magnitude


The *magnitude* or  *length* of a vector can be found in one of the following ways.
> Notation: $\|v\|$  meaning the magnitude of vector v

e.g. If the vector is in $\mathbb{R}^2$ and $\vec{v}=\langle2,3\rangle$:

$$\begin{align*}
\|\vec{v}\|&=\sqrt{2^2+3^2}\\
&=\sqrt{4+9}\\
&=\sqrt{13}
\end{align*}$$

Or similarly if the vector is in  $\mathbb{R}^3$ and $\vec{w}=\langle2,3,4\rangle$:

$$\begin{align*}
\|\vec{v}\|&=\sqrt{2^2+3^2+4^2}\\
&=\sqrt{4+9+16}\\
&=\sqrt{29}
\end{align*}$$

# Dot Product

A dot product is an operation that is performed on two different vectors which produces a constant or *scalar*.

**If the dot product of two vectors is $0$ the angle between them is [orthogonal](https://en.wikipedia.org/wiki/Orthogonality).**

The dot product has the following properties:
- Communitive | $u\cdot v = v\cdot u$
- Zero | $0\cdot v = 0$
- Distributive | $u\cdot (v + w) = u\cdot v + u\cdot w$
- Square | $u\cdot u = \|u\|^2$
- Constant Multiple | $c(u\cdot v) = cv\cdot u = v\cdot cu$

## Calculations

The dot product of two vectors is found as the following in $\mathbb{R}^2$: 

$$\langle i_{1}, j_{1}\rangle \cdot \langle i_{2}, j_{2}\rangle=
i_{1}*i_{2} + j_{1}*j_{2}$$

Or in $\mathbb{R}^3$: 

$$\langle i_{1}, j_{1}, k_{1}\rangle \cdot \langle i_{2}, j_{2}, k_{2}\rangle=
i_{1}*i_{2} + j_{1}*j_{2} + k_{1}*k_{2}$$

e.g. Given $v=\langle 1,2,3\rangle$ and $w=\langle 4,5,6\rangle$ 

$$\begin{align*}
v\cdot w &= 1*4  + 2*5 + 3*6\\
&=4 + 10 + 18\\
&=32
\end{align*}$$

The following formula can be manipulated to find the *angle between two vectors*:

$$\cos{\theta}=\frac{u\cdot v}{\|u\|\|v\|}$$

# Cross Product

A cross product is an operation performed between two different vectors which produces a resulting vector.

**The cross product of two vectors is always orthogonal to the two original vectors.**

## Calculations


The Co in $\mathbb{R}^3$: 

$$\langle i_{1}, j_{1}, k_{1}\rangle \cdot \langle i_{2}, j_{2}, k_{2}\rangle=
i_{1}*i_{2} + j_{1}*j_{2} + k_{1}*k_{2}$$
