This test involves a lot of assumptions about the series, so it should only be used when sure it would apply.

Given a series $\sum\limits_{n=0}^{\infty}a_n$ and a sufficently large $M$ if all three of the following conditions are met:
1. $a_n$ is **positive** for all $M\ge n$ 
2. $a_n$ is **decreasing** for all $M\ge n$
3. $a_n$ is **continous** for all $M\ge n$

The assuming $f(n)=a_n$ convergence of the series can be determined by the [[Integrals#Improper Integrals:|improper integral]]: $$\int_{n}^{\infty}f(n)dn$$
If $\int_{n}^{\infty}f(n)dn$ *diverges*, then $\sum\limits_{n=0}^{\infty}a_n$ *diverges* as well.
If $\int_{n}^{\infty}f(n)dn$ *converges*, then $\sum\limits_{n=0}^{\infty}a_n$ *converges* as well.
