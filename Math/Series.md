# Common Series:

## Geometric Series:

A geometric series is defined by the following:$$\sum\limits_{n=0}^{\infty}ar^n$$

If $a\ne0$ and $|r|<1$, then the geometric series *converges* to, $$\sum\limits_{n=0}^{\infty}ar^n=\frac{a}{1-r}$$where $a$ is equal to the first term of the sequence.

If $|r|\ge1$ the series *diverges*.

## P-Series:

A p-series is defined by the following:$$\sum\limits_{n=0}^{\infty}\frac{1}{n^p}$$where $p$ is any real constant.

If $p>1$ the series *converges*.
If $p\le1$ the series *diverges* 


# Convergence Tests:

Follow this order to help determine what test to use:

## 1. [[Nth Term Divergence Test]]:
This checks for general divergence, if the series does in fact diverge then no further work is needed. 

## 2. [[Ratio Test]] & [[Root Test]]
This is meant to deal with both positive and negative series, if for some reason they do not work or don't seem applicable move on to the next text

## 3. [[Comparison Tests]]
This is mostly helpful when you know of a larger p-series or geometric series that is similar to the series and it converges.

## 4. [[Integral Test]]
Try to avoid using this as it involves many assumptions but if you see a series that meets the criteria and is easily integrate able you can use this

## 5. [[Absolute Convergence]] & [[Alternating Series Test]] (For Negative Series)
Use these sparingly

# Power Series

A power series is an infinite series has a center $c$, radius of convergence $R$, and interval of convergence $I$.

The *radius* is defined by $$\left|x-c\right|<R$$

The *interval of convergence* is defined by $$(c-R,\space c+R)\quad \text{or}\quad[c-R,\space c+R]\quad \text{or}\quad (c-R,\space c+R]\quad \text{or}\quad [c-R,\space c+R)$$
This is because the series *may or may not* converge at the endpoints of the interval.

# Taylor Polynomials:

The idea behind a Taylor Polynomial is to extend the idea of linearization. This allows for a function to be approximated in the form of a polynomial, which is much easier to calculate and derive, and integrate.

A Taylor Polynomial is a partial sum of a [[#^3f36e4|Taylor Series]] that approximates the values of a function centered at a point $c$ up to a value $n$. $$T_n(x)=\sum\limits_{i=0}^{n}\frac{f^{(i)}(c)}{i!}(x-c)^i$$
This can also be represented as: $$T_n(x)=f(c)+\frac{f'(c)}{1!}(x-c)+\frac{f''(c)}{2!}(x-c)^2+\frac{f'''(c)}{3!}(x-c)^{3}...\frac{f^n(c)}{n!}(x-c)^n$$
## Maclaurin Polynomials:

This is just a Taylor Polynomial but the center $c$ is assumed to be 0.


# Taylor Series:

A Taylor Series is an infinite sum of a sequence that allows for the values of a function around a point by extending the idea of linearization around a center $c$.

It is given by the following: $$T(x)=\sum\limits_{n=0}^{\infty}\frac{f^{(n)}(c)}{n!}(x-c)^{n}$$
Finding the *Taylor Series* representation of a function is the same as finding the [[Series#Power Series|power series]] representation of a function. 

## Maclaurin Series:

This is just a Taylor Series but the center $c$ is assumed to be 0.

### Common Maclaurin Series:

$$e^x=\sum\limits_{n=0}^{\infty}\frac{x^n}{n!}$$ $R=\infty \quad I=(-\infty,\infty)$
- - - 
$$\arctan(x)=\sum\limits_{n=0}^{\infty}(-1)^{n}\frac{x^{2n+1}}{2n+1}$$ $R=1\quad I=(-1,1)$
- - - 
$$\frac{1}{1-x}=\sum\limits_{n=0}^{\infty}x^{n}$$ $R=1\quad I=(-1,1)$
- - -
$$\cos(x)=\sum\limits_{n=0}^{\infty}\frac{(-1)^nx^{2n}}{(2n)!}$$ $R=\infty\quad I=(-\infty,\infty)$
- - - 
$$\sin(x)=\sum\limits_{n=0}^{\infty}\frac{(-1)^{n}}{(2n+1)!}x^{2n+1}$$ $R=\infty \quad I=(-\infty, \infty)$
	