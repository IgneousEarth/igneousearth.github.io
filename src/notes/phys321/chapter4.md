# Chapter 4 - Electric Fields in Matter

> Reference "*Introduction to Electrodynamics*" by David Griffiths.

---

This chapter looks at electric fields within matter that aren't necessarily conductors - i.e.most matter in the universe. 
# Polarization

> Griffith's 4.1.

If we place a neutral atom in an electric field, the net force on it is zero (as it is uncharged) - *however*, the positively-charged nucleus is pushed along into the field, while the negatively charged electron cloud is pulled down into the field. 

![](images/chapter4/neutral-atom.svg)

The neutral atom is now **polarized**, with some tiny dipole moment $\vec{p}$:
$$
\vec{p} = \alpha \vec{E}
$$
$\alpha$ is the **atomic polarizability** and varies from atom to atom. 

> If the electric field is strong enough, the $e^-$ cloud will be ripped away from the nucleus and the atom will become ionized.

>Molecules become more complicated, since they're a few individual atoms coupled together - CO$_2$ for instance has different polarizabilities parallel or orthogonal to its axis ($\vec{p}=\alpha_\perp \vec{E}_\perp + \alpha_\parallel \vec{E}_\parallel$), so for molecules, a *polarization tensor* might be more useful.
>$$
\vec{p} = [p_x,p_y,p_z] = \begin{pmatrix}
\alpha_{xx}E_x & 0 & 0\\
0 & \alpha_{yy}E_y & 0\\
0 & 0 & \alpha_{zz}E_z
\end{pmatrix}
$$

## Force on dipoles

In the presence of an electric field, a dipole will rotate to point in the direction of the $E$-field with a torque given by
$$
\vec{N} = \vec{p}\times \vec{E}
$$
> At any other point on the dipole than the origin, $\vec{N} = (\vec{p}\times\vec{E}) + (\vec{r}\times \vec{F})$.


![](images/chapter4/dipole-rotation.svg)
The net force on a dipole in a uniform field is zero as seen in the first image. However, in a *non*uniform electric field, the force on a dipole is
$$
\vec{F} = (\vec{p}\cdot \vec{\nabla})\vec{E}
$$
The potential energy of a dipole in an electric field is
$$
U = -\vec{p}\cdot \vec{E}
$$

---

# The Field of a Polarized Object

> Griffiths 4.2.

In the presence of an external electric field, the individual atoms of a given material will become polarized, leading to a lot of little baby dipoles, all pointing in the direction of the applied field. 

Since all of its constituent atoms are polarized, the material itself is said to be polarized with some polarization density $\vec{P}$. 
$$
\vec{P} = \frac{\text{dipole moment}}{\text{unit volume}}
$$
## Potential

Since the potential for an individual dipole is 
$$
V(\vec{r}) = \frac{1}{4\pi\epsilon_0}\frac{\vec{p}}{\mathcal{R}^2}\hat{\mathcal{R}} = \frac{1}{4\pi\epsilon_0} \frac{\vec{p}}{|\vec{r}-\vec{r}'|^3}(\vec{r}-\vec{r'})
$$
The electric potential for the *entire* object with polarization $\vec{P}$ is
$$
V(\vec{r}) = \frac{1}{4\pi\epsilon_0}\int \frac{\vec{P}(\vec{r}')\cdot\hat{\mathcal{R}}}{\mathcal{R}^2}d\tau'
$$
With *surface* and *volume* **bound charge densities** of
$$
\sigma_b = \vec{P}\cdot\hat{n}\qquad \rho_b = -\vec{\nabla}\cdot\vec{P}
$$
We can rewrite the potential of our whole polarized object in terms of these densities:
$$
V(\vec{r}) = \frac{1}{4\pi\epsilon_0}\left[\oint_S \frac{\sigma_b}{\mathcal{R}}\;da' + \int_V\frac{\rho_b}{\mathcal{R}}\;d\tau' \right]
$$
> The net field is just the sum of the fields produced by the bound surface and volume charges. 

> $\vec{P}\cdot \hat{n} = P\cos\theta$, where $\theta$ is the angle between $\vec{P}$ and $\vec{n}$. 

## Physical interpretation of bound charge

> Griffiths'4.2.2 does an excellent job explaining this. I'm rehashing for my own education, but it's a good read for more detail.

Say we have a long string of dipoles, as we might in a polarized dielectric in some field $\vec{E}$. The head of one dipole will cancel the tail of its neighbor, *except* at the ends, so that:

![](images/chapter4/string-dipoles.svg)
No one electron makes the whole trip - but the magnitude of the $\Delta -$ in some field will be matched by $\Delta +$, such that it's almost conductor-like - in a *uniform field*, we see only accumulations of bound charge on the surface, such that
$$
\sigma_b = \vec{P}\cdot \hat{n} \equiv P\cos\theta \quad \text{(for some oblique surface)}
$$
If, however, the polarization is *non-uniform*, then we'll see accumulations of bound charge *within* the object, as well as on the surface, 
$$
\rho_b = -\vec{\nabla}\cdot \vec{P}
$$
