{% include mathjax.html %}

# Time Dependent Schröedinger Equation:

So far in our analysis we have only been looking at the spatial dependence of our eigenvectors, $\psi(x)$. To understand the behavior of any real quantum system we have to determine both it spatial and time dependence. This means that we have to find the complete wavefunction, $\Psi(x,t)$. To do so we have to solve the time dependent Schröedinger equation, TDSE:
<p align="center"> $H \Psi(x,t)= i \hbar \frac{\partial}{\partial t} \Psi(x,t)$, </p>
where the Hamiltonian operator $H$ is still the sum of the potential and kinetic energy and $i$ is the complex number defined as $i=\sqrt{-1}$ ([click here](/complexnumbers.md) for a quick refresher on complex numbers). In this derivation we are adopting the position basis for our energy eigenvectors, meaning that the Hamiltonian is also expressed in the position basis.

The TDSE cannot be analytically solved unless we can separate it into a time dependent term and a spatial dependent term. To do this, we need the help of an old trick called separation of variable technique where we can write the total wavefunction as:

<p align="center">  $\Psi(x,t)= \psi(x) T(t) $, </p>
where $\psi(x)$ is in the set of the solutions to the time independent Schröedinger equation $\{ {\psi(x)}_n \}$.

Therefore, the TDSE becomes:

<p align="center">  $H \psi(x) T(t)= i \hbar \frac{\partial}{\partial t}(\psi(x) T(t))$. </p>
We also know that the time dependent part is unchanged under the Hamiltonian (because $T(t)$ has no spatial dependence and H is basically a second derivative with respect to position) so the TDSE becomes

<p align="center">  $T(t) H \psi(x) = i \hbar \psi(x) \frac{\partial}{\partial t} (T(t))$. </p>

Now we can divide both sides by $\Psi(x,t)$. This cancels out some few terms and we are left with

<p align="center">  $\frac{H \psi(x) }{\psi(x) } = i \hbar \frac{1}{T(t)}\frac{\partial}{\partial t} (T(t)) $. </p>

Looking at the above equation, we can see that the left-hand side is only x-dependent while the right-hand side is only time-dependent. Mathematically, this is only possible if both sides are equal to one (the same) constant. We can already notice by looking at the left side of the equation that the constant has to be the energy $E$. Doing so, we get back our TISE

<p align="center">  $H \psi(x)_n=E \psi(x)_n$ </p>
and a second equation
<p align="center">$\frac{\partial}{\partial t} T(t)= \frac{-i E_n}{\hbar} T(t)$. </p>

We know how to deal with the TISE. So will not say more about that part in this page, instead we will try to focus on solving the time dependent part. 

First, lets rewrite it in a form ready for integration as follow:

<p align="center">  $\frac{dT}{T(t)}= (\frac{-i E_n}{\hbar}) dt $. </p>

Then integrating both sides, we obtain

<p align="center">  $\int_{0}^{T(t)}\frac{1}{T(t)}dT= \int_{o}^{t} (\frac{-i E_n}{\hbar}) dt $. </p>

So,
<p align="center">   $ln(T(t))=(\frac{-i E_n}{\hbar})t$. </p>

finally, 

<p align="center">  $T(t)= e^{(\frac{-i E_n}{\hbar})t}$. </p>

Putting everything together, we have $\Psi(x,t)=\psi(x)e^{(\frac{-i E_n}{\hbar})t}$. But we should not forget that this can only be achieved if the time and space dependence of the wavefunction are separable. So a good question to ask is when are they separable? and what does it mean, physically, to have the time and space functions separable?

It is important to notice that all physically realizable states are solutions to the TDSE but not all of them can be separated into a spatial and a time dependent functions. Only energy eigenfunction, in other words only the $\Psi(x,t)$ that satisfy the TISE, can be separated and therefore our derivations can only work for energy eigenfunctions. 

Now to understand the physical meaning of our derived separable function let's look at what the time-dependent part does.
We can use Euler formula to  obtain 

<p align="center"> $e^{\frac{-i E_n}{\hbar}t}= $ cos$ (\frac{ E_n}{\hbar}t) - i$ sin$ (\frac{ E_n}{\hbar}t)$. </p>

This represents a rotation in the complex plane with a frequency $\frac{E_n}{\hbar}$. The figure bellow shows what a rotation in the complex plane of the form $e^{i\theta t}$ looks like:

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/35788659-b433fafc-0a04-11e8-8652-6405e03fd2cb.jpg" width="500">
</p>

Notice that the frequency is dependent on the energy $E_n$, higher energy means faster rotation around the complex plane.
What this means for our wavefunction is that that, for a given energy, the energy eigenstate is the same overtime but it undergoes rotation around the complex plane. For this reason, we can refer to the energy eigenstate as a stationary state.

[Go back to home page](/README.md)
