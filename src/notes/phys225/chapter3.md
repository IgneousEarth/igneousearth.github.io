# Chapter 3 - Schrödinger Time Evolution

The time evolution of a quantum system is governed by the differential equation

$$ i\hbar\frac{d}{dt}\ket{\psi(t)} = H(t)\ket{\psi(t)} $$

where $H$ corresponds to the total energy of the system (the Hamiltonian operator, *different* from the Hermitian operator - though the Hamiltonian is still *a* Hermitian operator).

> **Postulate 6**
> The time evolution of a quantum system is determined by the Hamiltonian (total energy operator) $H(t)$, through the **Schrödinger equation**:
> $$ i\hbar\frac{d}{dt}\ket{\psi(t)} = H(t)\ket{\psi(t)} $$

The eigenvalues $E_n$ of the Hamiltonian are the *allowed energies* of the quantum system, and the eigenvectors (eigenstates) $\ket{E_n}$ are the energy eigenvectors of the system, such that
$$
H\ket{E_n} = E_n\ket{E_n}
$$
## The Energy Basis

Let's say we've already diagonalized $H$ and found values for the allowed energies $E_n$ and $\ket{E_n}$. General state vectors can be written in terms of these energy eigenstates:
$$ \ket{\psi(t)} = \sum_n c_n(t)\ket{E_n} $$
and, since the energy eigenvectors are orthonormal, we can write the **energy basis** as
$$
\braket{E_k|E_n} = \delta_{kn}
$$
Assuming the Hamiltonian $H(t)$ in this context is *time-independent*, such that $H(t_0) = H(t)$ for all $t$, then the time-dependent Schrödinger equation can be written
$$
\ket{\psi(t)} = \sum_n c_n e^{-iE_nt/\hbar}\ket{E_n} = \sum_n c_n e^{-i\omega_n t} \ket{E_n}
$$
where $\omega_n = E_n/\hbar$, an angular frequency. 
## Stationary States

Let's start with the simplest possible situation, where the quantum system is in one single energy eigenstate:
$$ \ket{\psi(0)} = \ket{E_1} $$
After some time $t$, this system will be in the state
$$ \ket{\psi(t)} = e^{-i\omega_1t} \ket{E_1} $$
where $\omega_1 = E_1/\hbar$. This state, however, differs from our initial state only by the phase factor $-i\omega_1 t$, and since phase changes will never affect the probability of measurements, the probability of observing some eigenvalue $a_j$ for an observable $A$ will be 
$$
\mathcal{P_{aj}} = |\braket{a_j|\psi(t)}|^2 = |\bra{a_j|e^{-i\omega_1t}\ket{E_1}}|^2 = |\braket{a_1|E_1}|^2
$$
This probability is *time-independent* and equal to the probability at $t_0$. There is no measurable time evolution for this state, and the energy eigenstates are called **stationary states** - if a system begins in some energy eigenstate, it will remain in that state. 

This same idea goes for multiple energy eigenstates:
$$ \ket{\psi(0)} = c_1\ket{E_1} + c_2\ket{E_2} $$
where
$$\mathcal{P}_{E_1} = |\braket{E_1|\psi(t)}|^2 \Rightarrow |c_1|^2$$

## Non-commuting Observables

If an observable $A$ commutes with $H$, then $A$ and $H$ have common eigenstates - so measuring $A$ is equivalent to measuring $H$. However, if $A$ does *not* commute with $H$, then the two observables will not share common eigenstates, and the eigenvalues of $A$ will be some superposition of energy eigenstates. 

Let the eigenstates of $A$ corresponding to $\ket{a_1}$ be represented by
$$\ket{a_1} = \alpha_1\ket{E_1} + \alpha_2\ket{E_2}$$
and the probability of measuring $a_1$ would be
$$ 
\begin{aligned}
	\mathcal{P}_{a_1} &= |\braket{a_1|\psi(t)}|^2\\
	&= |[\alpha_1^*\bra{E_1} + \alpha_2^*\bra{E_2}][c_1e^{-i\omega_1t}\ket{E_1}+c_2e^{-i\omega_2t}\ket{E_2}]|^2\\
	&= |a_1^*c_1e^{-i\omega_1t} + a_2^*c_2e^{-i\omega_2t}|^2
\end{aligned}
$$
The overall phase drops out - only the relative phase between $\omega_1$ and $\omega_2$ remains. 
$$ \omega_{21} = \frac{E_2-E_1}{\hbar} $$
which is the also **Bohr frequency**.

## Summary

In a time-dependent quantum system $\ket{\psi(t)}$ with a time independent Hamiltonian $H(t_0) = H(t)$, the probability of measuring $a_j$ of some observable $A$ at time $t$ can be found through the following process:

1. Diagonalize $H$ to find the eigenvalues $E_n$ and eigenvectors $\ket{E_n}$.
2. Write $\ket{\psi(0)}$ in terms of the energy eigenstates $\ket{E_n}$.
3. Multiply each eigenvector coefficient by $e^{-iE_nt/\hbar} = e^{-i\omega_n t}$ to get $\ket{\psi(t)}$ for some arbitrary $t$.
4. Calculate the probability $\mathcal{P}_{a_j} = |\braket{a_j|\psi(t)}|^2$.