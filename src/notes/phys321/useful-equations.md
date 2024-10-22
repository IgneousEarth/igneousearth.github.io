# Chapter 1

**Dot** **product identities**
$$
\vec{A}\cdot\vec{B} = AB\cos\theta
$$
$$
\vec{A}\cdot \vec{A} = A^2
$$
$$
\vec{A}\cdot\vec{B}=0\qquad \textrm{(if perpendicular)}
$$
---
**Cross** **product identities**
$$
\vec{A}\times\vec{B} = AB\sin\theta\;\hat{n}
$$
where $\vec{n}$ is the normal of the *plane formed* by the two vectors - follow the **right-hand rule** to find $\vec{n}$. 
$$
\vec{A}\times\vec{B} = \left| \begin{matrix}

\hat{x} & \hat{y} & \hat{z} \\
A_x & A_y & A_z\\
B_x & B_y & B_z

\end{matrix}\right|
$$
$$
\vec{A}\times\vec{B} = \vec{0}\qquad\text{(if parallel)}
$$
a *plane* has vector representation
$$
X\hat{x} + Y\hat{y}
$$

---
**Vector representation**
$$
\vec{A} = (A_x, A_y, A_z) \equiv A_x\hat{x}+A_y\hat{y}+A_z\hat{z}
$$
> $A_x$ is a *vector projection* of $\vec{A}$ along the $x$ coordinate axis, and same for the remaining three.

$$
\vec{r}=x\hat{x}+y\hat{y}+z\hat{z}\qquad \text{from origin to test point}
$$
$$
\vec{r}'=x'\hat{x}+y'\hat{y}+z'\hat{z}\qquad \text{from origin to source point}
$$
$$
\hat{r} = \frac{\vec{r}}{r} = \frac{x\hat{x} + y\hat{y}+z\hat{z}}{\sqrt{x^2+y^2+z^2}}
$$
$$
\mathcal{R} = \text{script r} = \vec{r} - r'\qquad\text{from test to source point}
$$
> $\vec{r}$ to **test point**
> $\vec{r}'$ to **location of charges**
> $\vec{\mathcal{R}}$ (script r) separation vector between the two

---

**Calculus**

Del operator
$$
\nabla = \vec{x}\frac{d}{dx} + \hat{y}\frac{d}{dy} + \hat{z}\frac{d}{dz}
$$
Divergence
$$
\nabla \cdot \vec{v} = \frac{dv_x}{dx} + \frac{dv_y}{dy} + \frac{dv_z}{dz}
$$
Curl
$$
\nabla \times \vec{v} = \left| \begin{matrix}
\hat{x} & \hat{y} & \hat{z}\\
d/dx & d/dy & d/dz\\
v_x & v_y & v_z
\end{matrix}\right| = \hat{x}\left(\frac{dv_z}{dy} -\frac{dv_y}{dz} \right)-\hat{y}\left(\frac{dv_x}{dz} -\frac{dv_z}{dx} \right) + \hat{z}\left(\frac{dv_y}{dx} -\frac{dv_x}{dy} \right)
$$

- Curl of gradient is zero $\nabla \times (\nabla f) = 0$
- Divergence of curl is also zero $\nabla \cdot (\nabla \times \vec{v}) = 0$
- Laplacian is divergence of gradient = $\nabla \cdot (\nabla f) = \nabla^2 f$

---

**Integrals**

Line (path) integral
$$
\int_\vec{a}^\vec{b} \vec{v}\cdot d\vec{l}\qquad \equiv \qquad \oint \vec{v}\cdot d\vec{l}\;\;\; \text{if a=b}
$$

Area integrals (in cartesian)
$$
\oint \vec{v}\cdot d\vec{a} = \oint \oint \vec{v}\cdot dxdy
$$
Volume integrals (of a scalar function)
$$
\int_V T\;d\tau = \int_V T\;dx\;dy\;dz
$$
for a vector-valued function, this might look like
$$
\int_V \vec{v}\;d\tau = \int(v_x\hat{x}+v_y\hat{y}+v_z\hat{z})\;d\tau = \hat{x}\int{v_x}\;d\tau + \hat{y}\int{v_y}\;d\tau + \hat{z}\int{v_z}\;d\tau
$$
---
**Theorems**

Fundamental theorem for gradients
$$
\int_{\vec{a}}^\vec{b} (\vec{\nabla}T)\;d\vec{l} = T(\vec{b}) - T(\vec{a})
$$
Green's theorem (Gauss's theorem)
$$
\int_V (\nabla \cdot \vec{v})\;d\tau = \oint_S \vec{v}\cdot d\vec{a}
$$
> Integral of a derivative over a region is equal to value of function at the boundary of that region - here, a surface integral over the volume's surface.

> $\oint$ is just $\int_{\vec{a}}^{\vec{b}=\vec{a}}$. 

Stokes theorem
$$
\int_S (\nabla \times \vec{v}) \cdot d\vec{a} = \oint_P \vec{v}\cdot d\vec{l}
$$
> RHS also called the *circulation* of $\vec{v}$.

