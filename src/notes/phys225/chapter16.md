# Chapter 16 - Quantum Computing

> In the 1980s, Feynman asked "Can a classical computer reliably model a quantum mechanical system?" - initially, the answer was no, since the **Hilbert space** scales based on the number $n$ of particles involved by a factor of $2^n$ ...
> 
> ... except ... nature does this *anyway*, regardless of the complexity involved. 

Thus, enter the quantum computer - at least, the idea of it. 

---

# Qubits - Quantum Bits

Classical computing uses binary digits (bits) to store information: 0 or 1. These numbers are strung together to represent larger numbers (1000101), but fundamentally use transistors that are either *on* or *off*.

In quantum information systems, information is stored in **quantum bits** (qubits) - a system with two possible states:
$$
\ket{0} = \ket{+}\qquad \ket{1} = \ket{-}
$$
The key difference is that qubits can exist in *superposition* states - where the state of the processor isn't only 0/1, but rather
$$
\ket{\psi} = c_0\ket{0}+c_1\ket{1} = \begin{pmatrix}c_0\\c_1\end{pmatrix}
$$
with *probabilities* of measuring each state as $|c_0|^2$ or $|c_1|^2$, as opposed to classically 100% either 0 or 1. As we include more qubits, we exponentially increase the information storage capacity of the system:
$$
\begin{aligned}
	\ket{00} &= \ket{0}_A\ket{0}_B\\
	\ket{01} &= \ket{0}_A\ket{1}_B\\
	\ket{10} &= \ket{1}_A\ket{0}_B\\
	\ket{11} &= \ket{1}_A\ket{1}_B
\end{aligned}
$$
and the general superposition state is
$$
\ket{\psi} = c_{00}\ket{00} + c_{01}\ket{01}+c_{10}\ket{10}+c_{11}\ket{11}
$$
For an $N$-qubit system, a single superposition state contains $2^N$ coefficients to represent information - compared to a *classical* system, where though $N$ bits has $2^N$ possible states, each state contains only $N$ bits of information.

> **However** - if we measure a state, the system state vector collapses from superposition onto the measured state vector - so we can only extract $N$ pieces of information from our system. We can get around this with **quantum parallelism**, as a consequence of quantum entanglement.

## Entangled States

The EPR state
$$
\ket{\psi} = \frac{1}{\sqrt{2}}(\ket{+}_1\ket{-}_2-\ket{-}_1\ket{+}_2)
$$
is **entangled** because measurements on one spin are perfectly anti-correlated with measurements on the other spin. It's the fourth of a set of **Bell states**, the complete set being
$$
\begin{aligned}
	\ket{\beta_{00}} &= \frac{1}{\sqrt{2}}(\ket{00}+\ket{11})\\
	\ket{\beta_{01}} &= \frac{1}{\sqrt{2}}(\ket{01}+\ket{10})\\
	\ket{\beta_{10}} &= \frac{1}{\sqrt{2}}(\ket{00}-\ket{11})\\
	\ket{\beta_{11}} &= \frac{1}{\sqrt{2}}(\ket{01}-\ket{10})\\
\end{aligned}
$$
This set is known as the **Bell basis**. Measuring one qubit in an entangled state affects the other (regardless of its location) instantaneously, allowing us to achieve the aforementioned parallel measurements - as long as we're clever about data organization. 

We can also have 2-qubit **product states** which are expressed as a product of 1-qubit states
$$
\ket{\psi} = (a_0\ket{0}_A+a_1\ket{1}_A)(b_0\ket{0}_B+b_1\ket{1}_B)
$$
> Quantum algorithms are not immune to the probabilistic nature of quantum mechanics - if the same program is run twice on a quantum computer the result may not be the same twice over. However, it allows us to produce answers in many, many fewer steps than a classical computer.
>
> This is why the idea of a **binary-quantum** processor is popular - both have strengths and weaknesses that each "half" makes up for.

