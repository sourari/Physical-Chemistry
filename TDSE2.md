{% include mathjax.html %}

# Time Dependent Schroedinger Equation for the Particle in a Box System:

In this section we want to numerically solve the TDSE for the PIB using Matlab.
At this stage, we only want to have an overall idea of the behavior of a particle inside an infinit 2-D square potential. So, we will set all the constant to a value of $1$ in Matlab as follow.

```Matlab
hbar=1;          %plank's constant
me=1;            %mass of electron
a=1;             %width of the box
barrht=10^6;     %hight of the barrier
pts=250;         %number of points discretizing space
barrier_width=3; %width of the barrier

```

From there, we can use the same code for the TISE to solve for the stationary states. Once we have the eigenvalues and eigenvectors for our Hamiltonian, we can multiply the eigenvectors $\psi_n(x)$ by the corresponding time-dependent function $T_n(t)= e^{(\frac{-i E_n}{\hbar})t}$ to obtain the total wavefunction $\Psi(x,t)$.
