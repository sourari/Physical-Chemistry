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

From there, we can use the same code we used for the TISE to solve for the stationary states. Once we have the eigenvalues and eigenvectors for our Hamiltonian, we can multiply the eigenvectors $\psi_n(x)$ by the corresponding time-dependent function $T_n(t)= e^{(\frac{-i E_n}{\hbar})t}$ to obtain the total wavefunction $\Psi_n(x,t)$. Once we obtain the energy eigenfunctions in position basis and normalize them we can use change of basis machinery we built in the previous sections to obtain the energy eigenvectors in enerfgy basis. Now we have all what is needed to plot the time evolution of these eigenstates. However, we will postpone this and calculate the probability density as well as the expectation value of the position x and energy E.

Calculating the probability density of the system is fairly straiforward and can be conputed using the following Matlab code.

```Matlab
Psi_E=zeros(pts,1);    %create empty eigenvector in E_basis
Psi_E(1)=1;            %define the energy state (here we took the first energy state)
for k=1:100                                  
 Psi_ET= Psi_E.*exp(-i*E*t/hbar); %Compute the time dependent eigenvector in E_basis
 Psi_XT=EtoX*Psi_ET;              %Compute the time dependent eigenvector in X_basis 
 Psi_XT=Psi_XT/norm(Psi_XT);               %normalize
 Proba_density= (conj(Psi_XT)).* Psi_XT;   %probability density in X_basis
end

```
However, the calculation of expectation value of x and E can be a little more treaky. We start with the expectation value of the position operator, $ < x > $. 
 Using position basis, we have $ < x > = < \Psi_x,\hat{x}\Psi_x > $. The expectation value of the position can also be computed using the energy basis as $ < x > = < \Psi_E,\hat{x}_E\Psi_E > $. Theoretically, this is feasible and will yield the exact same value as $ < \Psi_x,\hat{x}_x\Psi_x > $, i.e $ < x >_x = < x >_E $. However, computing the position operator matrix in energy basis is complicated and useless for our purpose since it will not add anything to our understanding of the system. Therefore, we will only work with the position basis for this part. To compute the position expectation value, we use the following Matlab code
  
  ```Matlab
Probability_density= (conj(Psi_XT)).* Psi_XT;

```

We use the same procedure for the energy by taking the expectation value of the Hamiltonian in position basis $ < H_x > = < \Psi_x, H_x \Psi_x> $ or in energy basis $ < \Psi_E, H_E \Psi_E > $. This time we can use either of the bases since we know that $H_E$ is the Vals matrix we computed for the PIB ([see here](/ChangeofBasis.md)) and we can go back and forth between $\Psi_x$ and $\Psi_E$ using the basis change machinery we derived in the [change of basis](/ChangeofBasis.md) section.

Now putting all of the above together, we can visualize the behavior of a particle in a box by plotting its energy eigenvectors in energy and position basis together with the probability density and expectation values.

<img src="https://user-images.githubusercontent.com/35305574/36699212-0506da5a-1b1a-11e8-9398-20a2d0a4969f.gif" width="500">


[Go back to home page](/README.md)
