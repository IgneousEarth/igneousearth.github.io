# Chapter 11 - Special Functions

> Reference *Mathematical Methods in the Physical Sciences* (3e) by Mary L. Boas. 

---

# Factorial functions $n!$

Factorial functions $n!$ are defined as
$$
n! = \int_0^\infty x^n e^{-x}\;dx
$$
More memorably, factorials are the product of their sums:
$$
5! = 5*4*3*2*1 = 120
$$
A table of the initial ones is below. 

| $n$ | $n!$ |
| --- | ---- |
| 0   | 1    |
| 1   | 1    |
| 2   | 2    |
| 3   | 6    |
| 4   | 24   |
| 5   | 120  |
# Gamma functions $\Gamma(n)$

For any $n>0$,
$$
\Gamma(n) = \int_0^\infty x^{n-1}e^{-x}
$$
The $\Gamma(n)$ is further easily defined in terms of factorials:
$$
\Gamma(n) = (n-1)!\qquad \Gamma(n+1) = n!
$$
Useful is also the *recursion relation*:
$$
\Gamma(n+1) = n\Gamma(n) = n(n-1)!
$$
> The gamma function seems useful for working with both fractions and complex numbers. 

For *negative* numbers where $n\leq 0$,
$$
\Gamma (n) = \frac{1}{n} \Gamma (n+1)
$$
Also, some special formulae:
$$
\begin{align*}
\Gamma(1/2) = \sqrt{\pi}\\
\Gamma(n)\Gamma(1-n) = \frac{\pi}{\sin(\pi n)}
\end{align*}
$$
**Note**: this last equation is undefined for integer $n=1,2,3\ldots$

# Beta functions $\beta(p,q)$

Beta functions, I'm not sure what they're useful for. But Boas gives several representations of it, which I'll include below. 

For $p,q>0$:
$$
\begin{align}
	\beta(p,q) &= \int_0^1 x^{p-1}(1-x)^{q-1}\;dx\\
	&= \frac{1}{a^{p+q-1}}\int_0^a y^{p-1}(a-y)^{q-1}\;dy\\
	&= 2\int_0^{2\pi} (\sin\theta)^{2p-1}(\cos\theta)^{2q-1}\;d\theta\\
	&= \int_0^{\infty} \frac{y^{p-1}}{(1+y)^{p+q}}\;dy
\end{align}
$$

Also, note that $\beta(p,q) = \beta(q,p)$.

In terms of gamma functions,
$$
\beta(p,q) = \frac{\Gamma{(p)}\Gamma{(q)}}{\Gamma(p+q)}
$$
