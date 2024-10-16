# Chapter 2 - Electrostatics

> Reference "*Introduction to Electrodynamics*" by David Griffiths.

---

Fundamentally, electrodynamics seeks to model the interaction of some set of charges $q_1, q_2, q_3$ on some other charge, $Q$. 
![](images/chapter2/source-on-test.svg)
We can do this via **superposition**, which states the interaction between two charges is *unaffected* by the presence of others - i.e. $\vec{F_1}$, the force between $q_1$ and $Q$, is independent of the presence of $q_2$ and $q_3$. We can then sum up the forces to get our net force on $Q$:
$$
\vec{F}_{\text{net}} = \vec{F_1}+\vec{F_2}+\vec{F_3}
$$
In an **electrostatic** system (no moving charges as opposed to an electrodynamic system), the forces can be calculated via *Coulomb's law*. 

## Coulomb's Law

Electrostatics simply takes into account distance and charge strength. Coulomb's law is

$$
\vec{F} = \frac{1}{4\pi\epsilon_0} \frac{qQ}{\mathbb{\mathcal{R}}^2}\hat{\mathbb{\mathcal{R}}}
$$
> $\epsilon_0$ is the permittivity of free space ($\epsilon_0=8.85\times10^{-12}$ $\text{C}^2/\text{N}\cdot\text{m}^2)$ and $\mathcal{R}=\vec{r}-\vec{r}'$ (Griffith's script-r).

in electrostatics, force increases with higher-magnitude charges, and decreases with distance.

![](images/chapter2/coulomblaw.png)
If we have *several* charges, we just sum their individual Coulomb forces as calculated above:

$$
\begin{aligned}
	\vec{F} &= \vec{F_1} + \vec{F_2} + \cdots\\
			&= \frac{Q}{4\pi\epsilon_0}\left( \frac{q_1}{\mathcal{R_1}^2}\hat{\mathcal{R_1}} + \frac{q_2}{\mathcal{R_2}^2}\hat{\mathcal{R_2}} + \cdots \right)
\end{aligned}
$$
In shorthand,
$$
\vec{F} = Q\vec{E}
$$
where $\vec{E}$, the **electric field**, is
$$
\vec{E} = \frac{1}{4\pi\epsilon_0}\sum_{i=1}^n \frac{q_i}{\mathcal{R_i}^2}\hat{\mathcal{R_i}}
$$
Note that the electric field is defined by the source charges present; it's more a model to represent the electric potential at various points, and what would happen if we dropped a test charge in. 

> $$ \epsilon_0 = 8.85\times10^{-12}\;\frac{C^2}{N\cdot{m}}$$

## Continuous Charge Distributions

If we have a set of charges $q_i$, then our electric field is a *discrete charge distribution*. If, however, the charge is distributed continuously over some region, then we have a *continuous charge distribution*.

![](images/chapter2/charge-distributions.png)
The electric field is then an integral over that continuous distribution:

$$
\vec{E}(\vec{r}) = \frac{1}{4\pi\epsilon_0} \int \frac{1}{\mathcal{R}^2}\hat{\mathcal{R}}\;dq
$$
where $dq$ varies for our continuous distribution type (1D, 2D or 3D), such that:
- **Line**:  $dq = \lambda(\vec{r}')\;dl'$
- **Area**: $dq = \sigma(\vec{r}')\;da'$
- **Volume**: $dq = \rho(\vec{r}')\;d\tau'$
# Divergence and Curl of Electrostatic Fields

> Griffiths 2.2.

---

**Field lines** are a way to visualize electric fields on a 2D or 3D medium. 

![](images/chapter2/field-lines.png)

> [Source](https://tikz.net/electric_fieldlines2/). 

where the **density** of field lines indicates the strength of the E-field at that location (strongest near the center in the above image). The flux of $\vec{E}$ through some surface $S$ is
$$
\phi_E = \int_S \vec{E}\cdot d\vec{a}
$$
and is a way to measure the **total charge** contained *within* a closed surface, while those *outside* of the surface don't affect it. 

![](images/chapter2/flux-thru-circle.png)

---

This mathematically represented by **Gauss's law**, which states
$$
\oint \vec{E}\cdot d\vec{a} = \frac{1}{\epsilon_0}Q_\text{enc}
$$
There's also a differential version of Gauss's law (found by applying the [Divergence Theorem](chapter1.md#Divergence)) where $\rho$ is charge density:
$$
\vec{\nabla} \cdot \vec{E} = \frac{1}{\epsilon_0}\rho
$$

---

For example in 3D, if a point charge $q$ is at the origin then the flux of $\vec{E}$ through a sphere around it is
$$
\oint \vec{E} \cdot d\vec{a} = \int \frac{1}{4\pi\epsilon_0} \left( \frac{1}{r^2}\hat{r} \right)\cdot (r^2 \sin\theta\;d\theta\;d\phi \hat{r}) = \frac{1}{\epsilon_0}q
$$
> We're only evaluating at the surface of the sphere, so $r$ is constant.

Note that Gauss's law is **only** useful with objects where the *E-field is pointing in the same direction as elements $d\vec{a}$*. This requires both a symmetrical charge distribution within the object, and for the Gaussian surface to be symmetric according to one of the following:

1. **Spherically symmetric** (concentric spheres)
2. **Cylindrically symmetric** (coaxial cylinders)
3. **Plane symmetric** (like a "box" that is cut in half by the plane)

The associated coordinate system is [used for each](chapter1.md#Curvilinear%20Coordinates).

**Note**: flux from *external charges is ignored*, since the flux entering a Gaussian surface from an external charge will be equal to the flux leaving that surface from the other side - hence, net flux from those external charges is zero. 

## Divergence of $\vec{E}$

$$
\begin{align}
\vec{\nabla}\cdot\vec{E} &= \frac{1}{4\pi\epsilon_0} \int \vec{\nabla}\cdot \left( \frac{\hat{\mathcal{R}}}{\mathcal{R}^2} \right)\rho(\vec{r}')\;d\tau'
\end{align}
$$
Since $\vec{\nabla}\cdot \left( \frac{\hat{\mathcal{R}}}{\mathcal{R}^2} \right) = 4\pi\delta^3(\vec{\mathcal{R}})$, then this just becomes
$$
\vec{\nabla}\cdot\vec{E} = \frac{1}{4\pi\epsilon_0}\int 4\pi\delta^3(\vec{r}-\vec{r}')\rho(\vec{r'})\;d\tau' = \frac{1}{\epsilon_0}\rho(\vec{r})
$$
Or, in shortform,
$$
\vec{\nabla}\cdot\vec{E} = \frac{1}{\epsilon_0}\rho(\vec{r})
$$
## Curl of $\vec{E}$

For **any** electrostatic charge distribution, the curl of the field is *always* zero.
$$
\vec{\nabla}\times \vec{E} = \vec{0}
$$

# Electric Potential $V$

> Griffiths 2.3.

---

Since $\nabla \times \vec{E} = 0$, the line integral around any closed loop is *zero* - thus, the line integral of $\vec{E}$ from point $\vec{a}$ to point $\vec{b}$ is the *same* *for* *all paths*. So we use a scalar $V$ that represents electric potential as a useful simplifying quantity. 

Electric potential $V$ is (by definition) path-independent, effectively representing a "displacement potential".
$$
V(\vec{r}) = -\int_{\mathcal{O}}^{\vec{r}} \vec{E}\cdot d\vec{l}
$$
and, flipped about, looks like
$$
\vec{E} = -\vec{\nabla}V
$$
