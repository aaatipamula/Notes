
This works best with polynomials in a fractional form and in the [[Limits#Indeterminate Forms|indeterminate form]] $\frac{0}{0}$. If the polynomial can be factored out so its multiples that are causing the denominator and numerator to take the form $\frac{0}{0}$ can be canceled out. 

Given $f(x)=\frac{x^2+x-6}{x^2-4}$ if asked to find $\lim_{x\to2}f(x)$ you can factor out the polynomial as such: $$\begin{align*}
\lim_{x\to2}\frac{x^2+x-6}{x^2-4}&=lim_{x\to2}\frac{(x-2)(x+3)}{(x-2)(x+2)}\\\
&=\lim_{x\to2}\frac{x+3}{x+2}
\end{align*}$$
 [[Direct Substitution]] can then be used to solve the limit: $$\lim_{x\to2}\frac{x+3}{x+2}=\frac{2+3}{2+2}=\frac{5}{4}$$
