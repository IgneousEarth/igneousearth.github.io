# Midterm 1 Study Guide

> Our first midterm is taking place 07/23/25, covering the content of the last 5 weeks of class. Here I will summarize my notes on those first 5 weeks to provide a review in preparation. 

---

# The Magnetic Field

Magnetic fields are caused by moving charges according to the Lorentz force law:
$$
\vec{F}_\text{mag} = Q(\vec{v}\times\vec{B} + \vec{E})
$$
> Many magnetostatic problems operate without $\vec{E}$ and it can often be ignored.

The direction of $\vec{B}$, $\vec{v}$ and $\vec{F}$ are all described by the right-hand rule. 

![](images/chapter5/rhr.svg)

Some notes on this:
- Currents in the same direction **attract**, in opposite directions **repel**.
- $\vec{v}$ more commonly represents $\vec{I}$, current.

Charged particles (ions) are attracted to magnetic field lines by a centripetal force given by the Lorentz law, and will orbit those field lines according to the **cyclotron formula**:
$$
QvB = m\frac{v^2}{R}\qquad \equiv \qquad p = QBR
$$
with a **cyclotron frequency** of 
$$\omega = \frac{QB}{m}$$
- If we have some parallel component $v_\parallel$ in addition to the perpendicular component $v_\perp$, the motion of the particle might look more like a helix.

## Calculating $\vec{B}$

$\vec{B}$ (without magnetization) is calculated either through the **Biot-Savart law**:
$$\vec{B}_I(\vec{r}) = \frac{\mu_0 I}{4\pi} \int \frac{d\vec{l}\times(\vec{r}-\vec{r}')}{|\vec{r}-\vec{r}'|^3}$$
>for surface current densities $\vec{K}$ or volume current densities $\vec{J}$:
>$$\vec{B}_K(\vec{r}) = \frac{\mu_0 K}{4\pi} \int \frac{d\vec{A'}\times(\vec{r}-\vec{r}')}{|\vec{r}-\vec{r}'|^3}\qquad \vec{B}_J(\vec{r}) = \frac{\mu_0 J}{4\pi} \int \frac{d\vec{\tau'}\times(\vec{r}-\vec{r}')}{|\vec{r}-\vec{r}'|^3}$$

$\vec{B}$ can also be calculated by **Ampère's law** (much nicer, but only if symmetry allows):
$$\oint \vec{B}\cdot d\vec{l} = \mu_0I_\text{enc}$$
- If we can infer the direction of $\vec{B}$, this can simplify to
$$B\oint dl = \mu_0 I_\text{enc}$$
- $\oint dl$ is some "Ampèrean loop" around the enclosed current. For a line of current, for example, it would be $\oint dl = 2\pi r$, the circumference of a circle where $r$ represents the radius at which we're measuring $B$. 

> $dl$ **must** point along magnetic field lines, such that the whole Ampèrean loop exactly lines up with magnetic field lines. Ampère's law therefore only works for:
> - Infinite straight lines / cylinders.
> - Infinite planes
> - Infinite solenoids
> - Toroids (wire wrapped around a donut)

See [equations](equations.md) for some $B$ fields for common objects.

---

# Current

Current represents charge per unit time passing through some cross-sectional area. 

For uniform current densities:
$$I = \lambda L = KA = J \tau$$
For nonuniform current densities:
$$I = \int K \cdot dl_\perp = \int J\cdot dA_\perp$$
> $dl_\perp$ and $dA_\perp$ represent lines and surfaces *orthogonal* to the direction of current flow respectively.

> Ex. If volume current density in a wire is proportional to the distance from the axis such as $\vec{J}=ks\hat{z}$, an orthogonal area is a circle with $da_\perp=s\;ds\;d\phi$, such that
> $$I = \int_0^R \int_0^{2\pi} (ks)(s\;ds\;d\phi) = \frac{2}{3}\pi ka^3$$
> $da=s\;ds\;d\phi$ is unitwise an area ($s\;d\phi$ is a unit arc length). 

# Magnetic Vector Potential $\vec{A}$

$$\vec{B} = \vec{\nabla} \times \vec{A}$$
$\vec{A}$ is an 'imaginary' definition such it is *defined* as the quantity of which $\vec{B}$ is a curl of. 

- Generally, *follows direction of current*.
- It is also divergenceless like $\vec{B}$ ($\vec{\nabla}\cdot \vec{A}=0$).

It has many properties; go see [equations](equations.md) to see them instantiated. $\vec{A}$ is hard to visualize and unintuitive to imagine. Just remember the above three ideas. 

# Boundary Conditions

If we have some field that is zero within/without a surface, and nonzero within/without that surface, then it must by nature have some **nonzero divergence**. 

Since $\vec{\nabla}\cdot \vec{B}=0$ ($\vec{B}$ is divergenceless), this means that $\vec{B}_\perp$ *must* be continuous across a boundary:
$$B^\perp_\text{inside} = B^\perp_\text{outside}$$
However, since the curl of $\vec{B}$ is allowed to be nonzero, the **parallel** (or tangential) components of $\vec{B}$ may have a discontinuity (such as zero inside and nonzero outside), *exactly* proportional to the *surface current density*:
$$B^\parallel_\text{inside} - B^\parallel_\text{outside} = \mu_0K\qquad \vec{B}_\text{inside} - \vec{B}_\text{outside} = \mu_0(\vec{K}\times\hat{n})$$

- Vector potential $\vec{A}$ is also continuous across a boundary. Its difference w.r.t. $\partial n$ is however also proportional to surface current density:
$$\frac{\partial\vec{A}_\text{inside}}{\partial n}-\frac{\partial\vec{A}_\text{outside}}{\partial n} = -\mu_0\vec{K}$$

---
# Magnetism

Every current loop has a **magnetic dipole moment**
$$m = I\int d\vec{a} = I\vec{a}$$
> $\vec{a}$ is the vector area of some Ampèrean loop.

![](images/chapter6/mag_moment.PNG)

In a magnetic field $\vec{B}$, dipoles *torque* instead of move:
$$\vec{N} = \vec{m}\times\vec{B}$$

## Magnetization

Magnetization $\vec{M}$ is the dipole moment per unit area of some material. 

- **Paramagnets**: magnetization *parallel* (same direction) as applied $\vec{B}$, odd # electrons.
- **Diamagnets**: magnetization *antiparallel* (opposite direction) to applied $\vec{B}$, even # electrons.
- **Ferromagnets**: magnetization persists even after the magnetic field has been removed.

> $\vec{M}$ is an "average" over a wildly complex set of infinitesimal dipoles and "smooths out" the dipole into a macroscopic view, useful for calculations.

> In a nonuniform field, generally paramagnets will be attracted into the field, diamagnets repelled away. 

For some magnetization, we tend to have **bound** charge densities now (which are electrons not free to scoot around). 
$$\vec{J_b} = \vec{\nabla}\times\vec{M}\qquad \vec{K_b} = \vec{M}\times\hat{n}$$
> $\vec{J_b}=0$ in a *uniform* magnetic field. Also, note $\vec{M}=0$ outside of a material.

- We can calculate $\vec{B}$ due to $\vec{M}$ by using Amp's law with $\vec{J}_b$ and $\vec{K_b}$ assuming symmetry. 
- This is also where magnetic vector potential really shines. See [equations](equations.md) for more on this.

# Auxiliary Field

This represents the "real world" field we see on an object - the sum of an object's magnetic field and magnetization, where
$$\vec{H} = \frac{1}{\mu_0}\vec{B} - \vec{M}$$
If we take the curl of this whole thing, we have corresponding charge densities for each.
$$\vec{\nabla}\times{\vec{H}} = \vec{J_f} \qquad \frac{1}{\mu_0}(\vec{\nabla}\times{\vec{B}}) = \vec{J}_\text{net} \qquad \vec{\nabla}\times{\vec{M}} = \vec{J_b}$$
Thus, 
$$\vec{J_f} = \vec{J}_\text{net} - \vec{J}_b$$
**Note on divergence**: since $\vec{\nabla}\cdot\vec{B}=0$,
$$\vec{\nabla}\times\vec{H} = -\vec{\nabla}\cdot\vec{M}$$

We can also use Ampère's law with $\vec{H}$. Since $\vec{\nabla}\times\vec{H}=\vec{J}_f$,
$$
\oint \vec{H}\cdot d\vec{l} = I_{f_\text{enc}}
$$
