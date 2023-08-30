# Definition:

The basic idea behind the an integral is to find the area under a curve of a function. This extends the idea of a [Reimann Sum](https://en.wikipedia.org/wiki/Riemann_sum) by creating infinitely small "rectangles" that we add up in order to get the area of a curve.

# Indefinite Integrals:

An *indefinite integral* is essentially the inverse operation to taking a [[Derivatives|derivative]], this may also known as an *anti-derivative*.

# Improper Integrals:

## Type 1: Infinite Bounds

This occurs when one of the bounds of an integral from $a$ to $b$ are equal to $\infty$.

This can be dealt with by reorganizing the integral's bounds. We will instead take the limit as a variable R goes to infinity and replace the infinity in the bound with R such that: 

$$\int_a^{\infty}f(x)dx=\lim_{R\to\infty}\int_a^Rf(x)dx$$

From there the integral can be solved as a proper integral keeping in mind the bound is a limit.

**Theorem 1:** the p-integral over $[a,\infty)$

## Type 2: Infinite Discontinuity

This is when there is an infinite break (usually a vertical asymptote sometimes another asymptote) in-between the bounds of the function to be integrated. 

This is dealt with by breaking the integral into two different parts and taking the limit where the function approaches the asymptote such that:

$$\int_{-2}^{2}\frac{1}{x}=\lim_{R\to0}\int_{-2}^{R}+\int_{R}^{2}$$

# Area Between Curves

There are two different types of areas, **Vertically Simple** and **Horizontally Simple**.

## Vertically Simple

If a vertical line is drawn and pushed through the area between two curves from $a$ to $b$ and:

1. The line touches both functions at exactly one point each.
2. One function's $y$ values are always greater than the other's on the interval ($a$,$b$)

the area is vertically simple.

ex.

![vertically simple](https://www.math.umd.edu/~petersd/241/html/ex19_01.png)


## Horizontally Simple

If a horizontal line is drawn and pushed through the area between two curves from *a* to *b* and:

1. The line touches both functions at exactly one point each.
2. One function's $x$ values are always greater than the other's on the interval (*a*,*b*)

the area is horizontally simple.

ex.

![horizontally simple](https://web.ma.utexas.edu/users/m408n/m408c/CurrentWeb/6-1-7_1.png)


## Finding the Area Between Curves

The area of a curve can be found by taking the integral of the outer function minus the inner function along the vertically or horizontally simple region's interval. 

e.g. Given $y=\sqrt{x}$ and $y=\frac{x}{2}$:

![[Pasted image 20230411152411.png]]

The area under the curve is: $$\int_{0}^{4}x^{2}-\frac{x}{2}dx$$

# Advanced Integration Techniques

## U-Substitution

This is mostly useful when solving simpler two product integrals in the form $\int{u(x)v(x)}dx$ where $u(x)$ or a subsequent "part" can be *substituted* by the derivative of $v(x)$ or vice versa.

e.g. Given $\int{\cos(x)\sin^2(x)}dx$  we could choose $u=\sin(x)$ which would make $du=\cos(x)dx$.

Substituting in $u$ and $du$ we come back with the equation:

$$\int u^2du$$

Which is a fairly simple integral to solve using the [[#Power Rule|power rule]]:

$$\begin{align*}
\int u^2du&=\frac{u^3}{3}+C\\
&=\frac{\sin^3(x)}{3}+C
\end{align*}$$

## Integration by Parts

