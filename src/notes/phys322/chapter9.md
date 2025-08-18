# Chapter 9 - Electromagnetic Waves

> Reference "*Introduction to Electrodynamics*" (5e) by David Griffiths.

---

Griffiths defines a wave as "*a disturbance of a continuous medium that propagates with a fixed shape at a constant velocity*".

If we represent such a wave mathematically, then we can say that the displacement $z$ (from the origin) at some later time $t$ is
$$f(z,t) = f(z-vt,0) = g(z-vt)$$
Or just 
$$f(z,t) = g(z-vt)$$
Solutions to this equation are determined via the **wave equation**. Let $u=z-vt$, such that $g(z-vt)=g(u)$. 
$$
\frac{d^2g}{du^2} = \frac{\partial^2 f}{\partial z^2} = \frac{1}{v^2}\frac{\partial^2f}{\partial  t^2}
$$
here the **speed of propagation** $v$ is given by 
$$v = \sqrt{\frac{T}{\mu}}$$
Functions of the form $g(z-vt)$ are not the only solutions - the wave equation has the square of $v$, so another class of solutions looks like $h(z+vt)$ - so the most general solution to the wave equation is
$$f(z,t) = g(z-vt)+h(z+vt)$$
> Note that this is a **linear** equation and 