# Useful Equations

Here are (most) of the equations I found useful in this class. 

---

# Dimensional analysis

> **Symbols**: [time](https://en.wikipedia.org/wiki/Time "Time") (T), [length](https://en.wikipedia.org/wiki/Length "Length") (L), [mass](https://en.wikipedia.org/wiki/Mass "Mass") (M), [electric current](https://en.wikipedia.org/wiki/Electric_current "Electric current") (I), [charge](https://en.wikipedia.org/wiki/Electric_charge)(Q = TI)

| Thing        | Dimensional units       |
| ------------ | ----------------------- |
| $\epsilon_0$ | $$\frac{T^4I^2}{ML^3}$$ |
| $E$          | $$\frac{ML}{T^3I}$$     |
| $V$          | $$\frac{ML^2}{T^{3}I}$$ |
| $F$          | $$\frac{ML}{T^2}$$      |
# Electrostatics

Coulomb's law (both $\vec{F}$ and $\vec{E}$)
$$
\vec{F} = \frac{1}{4\pi\epsilon_0} \frac{qQ}{\mathcal{R}^2}\hat{\mathcal{R}}\qquad \vec{E} = \frac{1}{4\pi\epsilon_0}\frac{q}{\mathcal{R}^2}\hat{\mathcal{R}}
$$
> **Notes**: 
> - $\vec{r}$ points from the origin to point we're interested in, $\vec{r'}$ from the origin to some 'unit charge' $dq$, thus $\vec{\mathcal{R}}=\vec{r}-\vec{r'}$.
> - $\vec{F}= Q\vec{E}$

Gauss's law
$$
\oint \vec{E}\cdot d\vec{a} = \frac{Q_\text{enc}}{\epsilon_0} \qquad  \vec{\nabla}\cdot \vec{E} = \frac{\rho}{\epsilon_0}
$$
