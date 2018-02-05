{% include mathjax.html %}

# Time Dependent Schroedinger equation:

So far in our analysis we have been only looking at the spacial dependence of our eigenvectors, $\psi(x)$. To understand the behavior of any real quantum system we have to determine both it spacial and time dependence. This means that we have to find the complete wavefunction, $\Psi(x,t)$. To do so we have to solve the time dependent Schroedinger equation, TDSE:
<p align="center"> $H \Psi(x,t)= i \hbar \frac{\partial}{\partial t} \Psi(x,t)$, </p>
where the Hamiltonian operator $H$ is still the sum of the potential and kinetic energy. In this derivation we are adopting the position basis for our wavefunction, meaning that the Hamiltonian is also expressed in the position basis.

The TDSE cannot be analytically solved unless we can separate it into a time dependent term and a spacial dependent term. To do this, we need the help of an old trick called separation of variable technique where we can write the total wavefunction as:

<p align="center">  $\Psi(x,t)= \psi(x) T(t) $, </p>
where $\psi(x)$ is in the set of the solutions to the time independent Schroedinger equation $\{ {\psi(x)}_n \}$.

Therefore, the TDSE becomes:

<p align="center">  $H (\psi(x) T(t))= i \hbar \frac{\partial}{\partial t} \psi(x) T(t)$. </p>
We also know that the time dependent part in unchanged under the Hamiltonian so 

<p align="center">  $T(t) H \psi(x) = i \hbar \psi(x) \frac{\partial}{\partial t} T(t)$. </p>

Now we can divide both sides by $\Psi(x,t)$, this cancels a few terms and are left with:

<p align="center">  $\frac{H \psi(x) }{\psi(x) } = i \hbar \frac{\frac{\partial}{\partial t} T(t)}{T(t)} $. </p>

Looking at the above equation, we can see that the left-hand side is only x-dependent while the right-hand side is only time-dependent. Mathematically, this is only possible if both sides are equal to one (the same) constant. We can already notice by looking at the left side of the equation that the constant has to be the energy $E$. Doing so, we get back our TISE

<p align="center">  $H \psi(x)_n=E \psi(x)_n$ and a second equation $\frac{\partial}{\partial t} T(t)= \frac{-i E_n}{\hbar} T(t)$. </p>

We know how to deal with the TISE. So will not say more about that part in this page, instead we will try to focus on solving the time dependent part. 

First, lets rewrite it in a form ready to integrate as follow:

<p align="center">  $\frac{dT}{T(t)}= (\frac{-i E_n}{\hbar}) dt $. </p>

Then taking integrating both sides we obtain

<p align="center">  $\int_{0}^{T(t)}\frac{1}{T(t)}dT= \int_{o}^{t} (\frac{-i E_n}{\hbar}) dt $. </p>

<p align="center">  So $ln(T(t))=(\frac{-i E_n}{\hbar})t$. </p>

finally, 

<p align="center">  $T(t)= e^{(\frac{-i E_n}{\hbar})t}$. </p>

Putting everything together, we have $\Psi(x,t)=\psi(x)e^{(\frac{-i E_n}{\hbar})t}$. But we should not forget that this can only be achieved if the time and space dependence of the wavefunction are separable. So w good question to ask is when are they separable and does that mean physically to have them separable?
