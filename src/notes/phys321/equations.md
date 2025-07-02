# Useful Equations

Here are (most) of the equations I found useful in this class. 

---

# Dimensional analysis

> **Symbols**: [time](https://en.wikipedia.org/wiki/Time "Time") (T), [length](https://en.wikipedia.org/wiki/Length "Length") (L), [mass](https://en.wikipedia.org/wiki/Mass "Mass") (M), [electric current](https://en.wikipedia.org/wiki/Electric_current "Electric current") (I), [charge](https://en.wikipedia.org/wiki/Electric_charge) (Q = TI), [energy](https://en.wikipedia.org/wiki/Energy) (T$^{-2}$L$^2$M)

| Thing          | Dimensional units      |
| -------------- | ---------------------- |
| $\epsilon_0$   | $$M^{-1}L^{-3}T^4I^2$$ |
| $1/\epsilon_0$ | $$ML^3T^{-4}I^{-2}$$   |
| $E$            | $$MLT^{-3}I^{-1}$$     |
| $V$            | $$ML^2T^{-3}I^{-1}$$   |
| $F$            | $$MLT^{-2}$$           |
| $C$            | $$M^{-1}L^{-2}T^4I^2$$ |
| $p$            | $$LTI$$                |

> Wikipedia's [dimensional analysis page](https://en.wikipedia.org/wiki/Dimensional_analysis#Simple_cases) has some other good simple cases. 
# Electrostatics

Coulomb's law (both $\vec{F}$ and $\vec{E}$)
$$
\begin{align}
	\vec{F} &= \frac{1}{4\pi\epsilon_0} \frac{qQ}{\mathcal{R}^2}\hat{\mathcal{R}}\qquad \vec{E} = \frac{1}{4\pi\epsilon_0}\frac{q}{\mathcal{R}^2}\hat{\mathcal{R}}\\
	 &\equiv \frac{1}{4\pi\epsilon_0} \frac{qQ}{\mathcal{R}^3}\vec{\mathcal{R}}\qquad \;\;\; \equiv \frac{1}{4\pi\epsilon_0}\frac{q}{\mathcal{R}^3}\vec{\mathcal{R}}
	
\end{align}
$$

> **Notes**: 
> - $\vec{r}$ points from the origin to point we're interested in, $\vec{r'}$ from the origin to some 'unit charge' $dq$, thus $\vec{\mathcal{R}}=\vec{r}-\vec{r'}$.
> 	- Imagine from one point charge to another.
> - $\vec{F}= Q\vec{E}$

Gauss's law
$$
\oint \vec{E}\cdot d\vec{a} = \frac{Q_\text{enc}}{\epsilon_0} \qquad  \vec{\nabla}\cdot \vec{E} = \frac{\rho}{\epsilon_0}
$$
# Multipole expansion

Monopole moment is total charge
$$
Q = \int dq\qquad V_\text{mon}(\vec{r}) = \frac{1}{4\pi\epsilon_0}\frac{Q}{r}
$$
Dipole moment points from south to north, origin-dependent
$$
\vec{\rho} = \sum_{i=1}^n q_i\vec{r}_i' \equiv \int \vec{r}'\;dq\qquad V_\text{dip}=\frac{1}{4\pi\epsilon_0}\frac{\vec{\rho}}{r^2}
$$
Quadrupole moment describes how charge dist. behaves in nonuniform fields
$$
Q_{ij} = \int \rho(\vec{r})\left(\frac{3}{2}r_ir_j - \frac{1}{2}r^2\delta_{ij} \right)\;d^3\vec{r}
$$

> $dq$, the charge integration element, is
> $$
dq = \begin{cases}
\lambda(\vec{r})\;dl & \quad\text{linear charges}\\
\sigma(\vec{r})\;da & \quad\text{surface charges}\\
\rho(\vec{r})\;d\tau & \quad\text{volume charges}
\end{cases}
$$

The electric potential for all multipole expansion terms is 
$$
V(\vec{r}) = \frac{1}{4\pi\epsilon_0}\sum_{n=0}^\infty \frac{1}{r^{n+1}}\int (r')^nP_n(\cos(\alpha))\;dq
$$
- $P_n$ represents the $n$th Legendre polynomial
- $\alpha$ is the angle between $\vec{r}$ and $\vec{r}'$

## Legendre polynomials

Calculated according to Rodrigues' formula:
$$
P_n(x) = \frac{1}{2^nn!}\frac{d^n}{dx^n}(x^2-1)^n
$$

| $n$ | $P_n(x)$                         |
| --- | -------------------------------- |
| 0   | $$1$$                            |
| 1   | $$x$$                            |
| 2   | $$\frac{1}{2}(3x^2-1)$$          |
| 3   | $$\frac{1}{2}(5x^3-3x)$$         |
| 4   | $$\frac{1}{8}(35x^4-30x^2+3)$$   |
| 5   | $$\frac{1}{8}(63x^5-70x^3+15x)$$ |

# Del operator

Due to unit vector and coordinate conversions, $\vec{\nabla}$ has [different representations](https://en.wikipedia.org/wiki/Del_in_cylindrical_and_spherical_coordinates) as applied in divergences as compared to normal functions. 

| Coordinate system | Gradient of $f$                                                                                                                                                                      | Dot product with $\vec{A}$                                                                                                                                                                                             |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Cartesian         | $$\vec{\nabla}f = \frac{\partial f}{\partial x}\hat{i}+\frac{\partial f}{\partial y}\hat{j} + \frac{\partial f}{\partial z}\hat{k}$$                                                 | $$\vec{\nabla}\cdot \vec{A} = \frac{\partial A_x}{\partial x}+\frac{\partial A_y}{\partial y} + \frac{\partial A_z}{\partial z}$$                                                                                      |
| Cylindrical       | $$\vec{\nabla}f = \frac{\partial f}{\partial r}\hat{r}+\frac{1}{r}\frac{\partial f}{\partial \phi}\hat{\phi} + \frac{\partial f}{\partial z}\hat{z}$$                                | $$\vec{\nabla}\cdot \vec{A} = \frac{1}{r}\frac{\partial (rA_r)}{\partial r}+\frac{1}{r}\frac{\partial A_\phi}{\partial \phi} + \frac{\partial A_z}{\partial z}$$                                                       |
| Spherical         | $$\vec{\nabla}f = \frac{\partial f}{\partial r}\hat{r}+\frac{1}{r}\frac{\partial f}{\partial \theta}\hat{\theta} + \frac{1}{r\sin\theta}\frac{\partial f}{\partial \phi}\hat{\phi}$$ | $$\vec\nabla\cdot\vec{A} = \frac{1}{r^2}\frac{\partial}{\partial r}(r^2A_r) + \frac{1}{r\sin\theta}\frac{\partial}{\partial \theta}(A_\theta\sin\theta) + \frac{1}{r\sin\theta}\frac{\partial A_\phi}{\partial \phi}$$ |
