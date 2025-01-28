# Chapter 6 - Magnetic Fields in Matter

> Reference "*Introduction to Electrodynamics*" (5e) by David Griffiths.

---

If a material is placed in a $\vec{B}$-field, it will acquire a *magnetic polarization* (or **magnetization**). Different materials acquire different polarizations depending on their atomic structures.

- **Paramagnets**: magnetization *parallel* to applied $\vec{B}$, materials with odd # of electrons. 
- **Diamagnets**: magnetization *antiparallel* to applied $\vec{B}$, materials with an even # of electrons.
- **Ferromagnets**: magnetization persists on the material even after the applied $\vec{B}$-field is removed, and is determined by the whole "magnetic history" of the object.

> All electrons act as magnetic dipoles.

> Imagine a magnetic dipole as pointing from south to north (the Gilbert model). It's an inaccurate model at small scales according to Griffiths, but he recommends it for intuition. 

![](images/chapter6/mag_moment.PNG)

## Torques and Forces on Magnetic Dipoles

Magnetic dipoles will experience some torque $N$ in an applied field, where 
$$
\vec{N} = \vec{m}\times\vec{B}
$$
and $m$ is the magnetic dipole moment. For paramagnetic materials (odd electrons), $m$ will be roughly in the same direction as the applied $\vec{B}$-field.

For a current loop, $m=Iab$ where $a,b$ are side lengths. 

> In a uniform field the net force on the dipole is zero, though this is not the case for nonuniform fields. 

For an *infinitesimal* loop with dipole moment $\vec{m}$ in field $\vec{B}$, the force on the loop is
$$
\vec{F} = \nabla (\vec{m}\cdot \vec{B})
$$

## Diamagnets

Diamagnetism affects *all* materials, but is much weaker than paramagnetism, so is most easily observed in materials with an *even* number of electrons.

When an external $\vec{B}$-field is applied to a material, individual electrons will speed up according to
$$
\Delta v = \frac{eRB}{2m_e}
$$
where $R$ is the "radius" of the electron from the nucleus of an atom. This increase in orbital speed will change the dipole moment
$$
\Delta \vec{m} = -\frac{1}{2}e(\Delta v)(R)\hat{z} = -\frac{e^2R^2}{4m_e}\vec{B}
$$
this change in the dipole moment is **antiparallel** to $\vec{B}$ as shown above. 

## Magnetization

Magnetization $\vec{M}$ is
$$
\vec{M} = \text{magnetic dipole moment }\vec{m} \text{ per unit volume}
$$
For a paramagnet, perhaps suspended above a solenoid, the magnetization would be positive/upward, and force downward. For a diamagnet, the magnetization would be instead downward, and force upward. 

> In general in a *non*uniform field, paramagnets are attracted into the field, and diamagnets are repelled away. 

**Note**: $\vec{M}$ is an *average* over a wildly complex set of infinitesimal dipoles and "smooths out" the dipole into a macroscopic view.

**Note**: both diamagnetism and paramagnetism are quite *weak* compared to, for instance, ferromagnetism, and so are often neglected in experimental calculations. 

# Field of a Magnetized Object

For some single dipole, the magnetic vector potential is
$$
\vec{A}(\vec{r}) = \frac{\mu_0}{4\pi} \frac{\vec{m}\times{\hat{R}}}{R^2}
$$
For a magnetized object with magnetization $\vec{M}$,
$$
\vec{A}(\vec{r}) = \frac{\mu_0}{4\pi} \int \frac{\vec{M}(\vec{r}')\times\hat{R}}R^2
d\tau'$$
Alternatively, we can look at the object in terms of its volume current density $\vec{J}_b$ and surface current density $\vec{K}_b$, where
$$
\vec{J}_b = \nabla\times\vec{M}\qquad \vec{K}_b = \vec{M}\times\hat{n}
$$
$$
\vec{A}(\vec{r}) = \frac{\mu_0}{4\pi} \int_V \frac{\vec{J}_b(\vec{r}')}{R}d\tau'+\frac{\mu_0}{4\pi} \oint_S \frac{\vec{K}_b(\vec{r}')}{R}dA'
$$
> This means the potential (and therefore magnetic field) is the same as would be made by some volume current $\vec{J}_b$ throughout the material plus the surface current $\vec{K}_b$ on the boundary.
>
> This means we needn't integrate all the infinitesimal dipoles, but rather just determine the **bound currents** $\vec{J}_b$ and $\vec{K}_b$ and find the field they produce. 

**Note**: $\nabla \cdot \vec{J}_b = 0$ 