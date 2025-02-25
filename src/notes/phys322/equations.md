# Useful Equations

Here are (most) of the equations I found useful in this class. 

---

# Magnetic Fields

$$
\begin{align*}
	\oint \vec{B}\cdot d\vec{l} = \mu_0 I_\text{enc}\qquad& \text{$d\vec{l}$ along $\vec{B}$ (Ampere's law)}\\
\end{align*}
$$
$$
\begin{align*}
	\vec{B}(\vec{r}) &= \frac{\mu_0}{4\pi} \int \frac{I\times \hat{R}}{|R|^2} dl' \qquad\text{Biot-Savart law}\\
	&\equiv \frac{\mu_0}{4\pi}I \int\frac{d\vec{l}\times \hat{R}}{|R|^2}\qquad\text{if constant $I$}
	
\end{align*}
$$
> $\vec{r}$ from origin to test point, $\vec{r}'$ origin to test charge $d\vec{l}$, $\vec{R}=\vec{r}-\vec{r}'$ (Griffiths' script-r)

| Scenario (current $I$)                            | Field                                                                                                          | Griffiths ref. |
| ------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------- |
| Solenoid running along $+z$, $n$ turns per length | $$\vec{B}_\text{sol} = \begin{cases} \mu_0nI\hat{z}\quad& \text{inside}\\ 0\quad &\text{outside} \end{cases}$$ | 5.59           |
| Long straight wire of radius $R$                  | $$\vec{B}_\text{wire} = \frac{\mu_0 I}{2\pi r}\hat{\phi}$$                                                     | 5.39           |

# Magnetism

Force
$$
\begin{align*}
	\vec{F} = q(\vec{E} + \vec{v}\times\vec{B})\qquad&\\
	\vec{F}_{\text{loop}} = I\oint (d\vec{l}\times\vec{B}) = 0\qquad &\text{uniform $\vec{B}$}\\
	\vec{N} = \vec{m}\times\vec{B}\qquad&
\end{align*}
$$

> For an electron $\Delta \vec{m} = -\frac{e^2R^2}{4m_e}\vec{B}$.

Auxiliary field $\vec{H}$
$$
\begin{align*}
	\vec{H} = \frac{1}{\mu_0}\vec{B}-\vec{M}\\
	\vec{B} = \mu_0(1+\chi_m)\vec{H}\\
	\vec{B} = \mu \vec{H}\\
	\vec{M} = \chi_m\vec{H}\\
	\vec{\nabla} \cdot \vec{H} = -\vec{\nabla}\cdot \vec{M}
\end{align*}
$$
> $\chi_m$ is magnetic susceptibility, $\mu=\mu_0(1+\chi_m)$ is permeability

$\vec{M}$:
$$
\begin{align*}
	\vec{M} = \frac{1}{\mu_0} \vec{B}\left( 1 - \frac{1}{1+\chi_m} \right)\\
	\vec{M} = \vec{B}\left(\frac{1}{\mu_0} - \frac{1}{\mu}\right)
\end{align*}
$$

Current densities $\vec{J},\;\vec{J}_b$ and $\vec{J}_f$ and surface density $\vec{K}_b$:
$$
\begin{align*}
	\vec{J} = \vec{J}_b+\vec{J}_f\\
	\vec{J}_f = \vec{\nabla}\times\vec{H} \\
	\vec{J}_b = \vec{\nabla}\times\vec{M} \\
	\vec{\nabla}\cdot \vec{J}_b = 0\\
	\frac{1}{\mu_0}(\vec{\nabla}\times\vec{B}) = \vec{J}\\
	\vec{K_b} = \vec{M}\times \hat{n}
\end{align*}
$$
> $\vec{J}_b=0$ if uniform $\vec{M}$. 

> Divergence of curl is *always* zero. 

Magnetic vector potential $\vec{A}(\vec{r})$
$$
\begin{align*}
	\vec{A}(\vec{r}) = \frac{\mu_0}{4\pi}\frac{\vec{m}\times\hat{R}}{R^2}\qquad &\text{single dipole}\\
	\vec{A}(\vec{r}) = \frac{\mu_0}{4\pi} \int \frac{\vec{M}(\vec{r}')\times\hat{R}}{R^2}d\tau \qquad & \text{magnetized obj}\\
	\vec{A}(\vec{r}) = \frac{\mu_0}{4\pi}\left[\int_V \frac{\vec{J}_b(\vec{r}')}{R}d\tau'  + \oint_S \frac{\vec{K}_b(\vec{r}')}{R}da' \right] \qquad& \text{mag. obj. J \& K}
\end{align*}
$$
# Electrodynamics

Current density $\vec{J}$:
$$
\begin{align*}
	\vec{J} = \sigma \vec{f}\qquad\\
	\vec{J} = \sigma \vec{E}\qquad &\text{if $\vec{v}$ small}\\
	E = \frac{V}{d}\qquad&\text{between 2 plates}\qquad&\\
	P = VI = I^2R\qquad&\text{Joule heating law}
\end{align*}
$$
> $I$ is current, $\vec{J}$ current density, $I=J*A$. 

Electromotive force $\epsilon$:
$$
\begin{align*}
	\epsilon = \oint \vec{f}\cdot d\vec{l} = \oint \vec{f}_s
	\cdot d\vec{l} \qquad&\\
	\vec{f} = \vec{f}_s+\vec{E}\qquad&\\
	
\end{align*}
$$

# Dimensional analysis

> **Symbols**: [time](https://en.wikipedia.org/wiki/Time "Time") (T), [length](https://en.wikipedia.org/wiki/Length "Length") (L), [mass](https://en.wikipedia.org/wiki/Mass "Mass") (M), [electric current](https://en.wikipedia.org/wiki/Electric_current "Electric current") (I)

| Thing                              | Dimensional units       |
| ---------------------------------- | ----------------------- |
| $\mu_0$                            | $$\frac{ML}{T^2I^2}$$   |
| $\vec{B}$                          | $$\frac{M}{T^2I}$$      |
| $\vec{M}$ & $\vec{H}$              | $$\frac{I}{L}$$         |
| $\vec{J}$                          | $$\frac{I}{L^2}$$       |
| $R$ ($\Omega$)                     | $$\frac{ML^2}{T^3I^2}$$ |
| $\sigma$ (conductivity)            | $$\frac{T^3I^2}{ML^3}$$ |
| $\epsilon_0$ (vacuum permittivity) | $$\frac{T^4I^2}{ML^3}$$ |
