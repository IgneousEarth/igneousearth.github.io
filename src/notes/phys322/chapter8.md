# Chapter 8 - Conservation Laws

> Reference "*Introduction to Electrodynamics*" (4e) by David Griffiths.

---

The mathematical equation for local conservation of charge (better known as the **continuity equation**) is
$$\frac{\partial \rho}{\partial t} = -\vec{\nabla}\cdot \vec{J}$$

# Poynting's Theorem

The *total energy* stored in electromagnetic fields is
$$u = \frac{1}{2}\left(\epsilon_0 E^2 + \frac{1}{\mu_0}B^2\right)$$
**Poynting's theorem** reads "the work done on charges by the electromagnetic force is equal to the decrease in energy remaining in the fields, minus the energy that flowed out through the surface". 

It's easier represented by the **Poynting vector**:
$$
\vec{S} = \frac{1}{\mu_0}(\vec{E}\times\vec{B})
$$
which represents the *energy per unit time, per unit area* or **energy flux density**. 
> $\vec{S}$ represents the *movement of energy* or transfer of energy, and will point in the direction of this transfer.

The continuity equation for energy is
$$\frac{\partial u}{\partial t} = -\vec{\nabla}\cdot\vec{S}$$

---

# Momentum

Electromagnetic fields *themselves* carry momentum (bizarrely enough). 

Imagine firing a gigantic laser beam from Earth at some spacecraft:

![](images/chapter8/solar-sail.svg)The barrage of photon would cause the solar sail spacecraft to accelerate. This is the principle behind the [Breakthrough starshot](https://en.wikipedia.org/wiki/Breakthrough_Starshot) project. The only way this is possible is if the photons (i.e. the E/M waves themselves) carried some momentum.

> **Note on Newton's Third**: in electrodynamics, *Newton's third law* (equal and opposite) does not always hold. 


## Maxwell stress tensor

The **Maxwell stress tensor** is used to relate electromagnetic forces and mechanical momentum, and is the *force per unit area* (or *stress*) acting on the surface. 
$$
T_{ij} \equiv \epsilon_0\left( E_iE_j-\frac{1}{2}\delta_{ij}E^2 \right) + \frac{1}{\mu_0}\left( B_iB_j - \frac{1}{2}\delta_{ij}B^2 \right)
$$
> The Kronecker delta $\delta_{ij}$ is 1 if the indices are the same, zero otherwise, such that (for example):
> $$\begin{align}
T_{xx} &= \frac{1}{2}\epsilon_0(E_x^2-E_y^2-E_z^2)+\frac{1}{2\mu_0}(B_x^2-B_y^2-B_z^2)\\
T_{xy} &= \epsilon_0(E_xE_y)+\frac{1}{\mu_0}(B_xB_y)
\end{align}$$

The stress tensor can be written in two ways, both equivalent - the double arrow is used to indicate it's a vector with more than one index. 

$$T_{ij} \equiv \overleftrightarrow{T}$$
The dot product of the tensor can only operate under one index:
$$(T_{ij}\cdot \vec{a})_j = \sum_{i={x,y,z}} T_{ji}a_i$$
The *divergence* of the stress tensor is ... long, but below.
$$
\begin{aligned}
(\vec{\nabla}\cdot T_{ij})_j = \epsilon_0\left[ (\vec{\nabla}\cdot\vec{E})E_j+(\vec{E}\cdot\vec{\nabla})E_j-\frac{1}{2}\vec{\nabla}_jE^2 \right]\\
+\frac{1}{\mu_0}\left[ (\vec{\nabla}\cdot\vec{B})B_j+(\vec{B}\cdot\vec{\nabla})B_j-\frac{1}{2}\vec{\nabla}_jB^2 \right]
\end{aligned}
$$

---

The **electromagnetic force per unit volume** $\vec{f}$ can be written
$$
\vec{f} = \vec{\nabla}\cdot T_{ij} - \epsilon_0\mu_0\frac{\partial\vec{S}}{\partial t}
$$
and the *total* electromagnetic force on some charges in some volume $V$ is
$$
\vec{F} = \oint_S T_{ij}\cdot d\vec{a} - \epsilon_0\mu_0\frac{d}{dt}\int_V \vec{S}\;d\tau
$$
In the *static* case (i.e. $\vec{E}\times\vec{B}$ does not vary with time),
$$\vec{F} = \oint_S T_{ij}\cdot d\vec{a}$$

---

In an applied context, $T_{ij}$ is the force per unit area, in the $i$th direction, acting on an element of surface in the $j$th direction. 

So,
- $T_{xx},T_{yy}, T_{zz}$ represent *pressures*.
- $T_{xy}, T_{xz},$ etc. represent *shears*.

## Conservation of Momentum

Newton's second (in another form) says the force on an object is the rate of change in its momentum:
$$\vec{F} = \frac{d\vec{p}}{dt}$$
The **conservation of momentum** in electrodynamics is therefore
$$
\frac{d\vec{p}}{dt} = -\epsilon_0\mu_0\frac{d}{dt}\int_V \vec{S}\;d\tau + \oint_S T_{ij}\cdot d\vec{a}
$$
Griffiths' interpretation says the **momentum stored in the E/M fields** is 
$$\vec{p} = \mu_0\epsilon_0\int_V\vec{S}\;d\tau$$
while the second integral is the *momentum per unit time, flowing into the volume through the surface*.

The **momentum density**, or momentum per unit volume, is
$$\vec{g} = \mu_0\epsilon_0\vec{S} = \epsilon_0(\vec{E}\times\vec{B})$$
And the continuity equation for momentum is 
$$\frac{\partial \vec{g}}{\partial t} = \vec{\nabla}\cdot T_{ij}$$