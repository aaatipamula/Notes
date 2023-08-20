This method of calulating limits works best with *two polynomials in fractional form*.

Given the limit: $$\lim_{x\to\infty}\frac{4x^3+6x^2+4}{8x^6+x^4+7x+1}$$ [[L'Hopitals Rule]] could be used, however it would be impractical to take that many derivatives.

Instead we take the highest order term from the polynomial in the numerator and divide the terms in the numerator and denominator by that Nth degree term which in the case of this limit is $x^4$ so: $$\lim_{x\to\infty}\frac{4x^3+6x^2+4}{8x^6+x^4+7x+1}=\lim_{x\to\infty}\frac{4+\frac{6}{x}+\frac{4}{x^3}}{8x^3+x+\frac{7}{x^2}+\frac{1}{x^3}}$$
With this form we can [[Direct Substitution|direct substitute]] and get our answer which would be 0 in this case.