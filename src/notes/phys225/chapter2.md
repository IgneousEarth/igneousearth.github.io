# Chapter 2 - Operators & Measurement

> Reference *Quantum Mechanics: A Paradigms Approach* by David McIntyre.

---

**Operators** are mathematical objects that operate on kets to turn them into new kets; $S_z$ is one such example. 
$$
A\ket{\psi} = \ket{\phi}
$$
If a ket is *not* changed by the application of some operator, then the ket is known as an **eigenvector** and the associated constants are **eigenvalues**. 
$$
A\ket{\psi} = a\ket{\psi}
$$
Above, $\ket{\psi}$ is the eigenvector and $a$ is an eigenvalue. Both eigenvectors and eigenvalues are properties of the operator $A$ - if it changes, so does the eigenstuff. For the operator $S_z$, the eigenvectors / values are:
$$
S_z\ket{+} = +\frac{\hbar}{2}\ket{+}\qquad S_z\ket{-} = -\frac{\hbar}{2}\ket{-}
$$
> **Postulate 3**: The only possible result of a measurement of an observable (like $S_z$) is one of the eigenvalues $a_n$ of the corresponding operator $A$.

This postulate implies that, if we have the eigenvectors and values of $A$, we can actually reconstruct $A$ from them.

Let $S_z \equiv \begin{pmatrix} a & b \\ c & d \end{pmatrix}$.
$$
S_z\ket{+} = +\frac{\hbar}{2}\ket{+}\qquad \begin{pmatrix} a & b \\ c & d \end{pmatrix}\begin{pmatrix}1\\0\end{pmatrix} = +\frac{\hbar}{2}\begin{pmatrix}1\\0\end{pmatrix}
$$
$$
S_z\ket{-} = -\frac{\hbar}{2}\ket{-}\qquad \begin{pmatrix} a & b \\ c & d \end{pmatrix}\begin{pmatrix}0\\1\end{pmatrix} = -\frac{\hbar}{2}\begin{pmatrix}0\\1\end{pmatrix}
$$
Which leads us to
$$
\begin{pmatrix}
a\\ c
\end{pmatrix} = +\frac{\hbar}{2}\begin{pmatrix}1\\0\end{pmatrix}\qquad \begin{pmatrix}
b\\ d
\end{pmatrix} = -\frac{\hbar}{2}\begin{pmatrix}0\\1\end{pmatrix}
$$
Now, plugging these solved values in,
$$
S_z \equiv \begin{pmatrix}
\hbar/2 & 0\\
0 & -\hbar/2
\end{pmatrix} = \frac{\hbar}{2}\begin{pmatrix}
1 & 0\\
0 & -1
\end{pmatrix}
$$
1. Operators are **diagonal** in their own basis (i.e. they only have elements along the main diagonal). 
2. The elements along the diagonal are the **eigenvalues** of the operator. 
	- The eigenvectors themselves are not included in the operator matrix.

> **Note**: an *observable* is some physical quantity that can be measured - such as spin. In that context, the operator $S_z$ represents that observable. 

## Other representations

We can also represent an operator matrix $A$ in terms of its elements. Let the operator $A$ describe some two-dimensional spin-1/2 system (like $S_z$ does).

$$
A \equiv \begin{pmatrix}
a & b\\
c & d
\end{pmatrix} = \begin{pmatrix}
\braket{+|A|+} & \braket{+|A|-} \\
\braket{-|A|+} & \braket{-|A|-}
\end{pmatrix}
$$
Where
$$
\braket{+|A|+} = \begin{pmatrix}1 & 0\end{pmatrix}\begin{pmatrix}
a & b\\
c & d
\end{pmatrix}\begin{pmatrix}1 \\ 0\end{pmatrix} = a
$$
## Finding eigenvectors / values from an observable

If we know the operator $A$, and need to find the possible results of a measurement of the corresponding observable, we can start from the general eigenvalue equation and work from there.

$$
A\ket{\lambda} = \lambda\ket{\lambda}
$$
where $\lambda$ is the eigenvalue and $\ket{\lambda}$ is the corresponding eigenvector. Eigenvalues can be found then by solving the *secular equation*,
$$
\det|A - \lambda I| = 0
$$
**Note**: for a $2\times2$ operator (i.e. a spin-1/2 system), this is $ad-bc=0$.

After finding the eigenvalues, we now know $A$ and $\lambda$ - all that remains is to find $\ket{\lambda}$ by solving for it in $A\ket{\lambda} = \lambda\ket{\lambda}$. 

> The process of finding the eigenvectors and eigenvalues of a matrix is known as **diagonalization**. 