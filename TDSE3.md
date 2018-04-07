{% include mathjax.html %}


## Perturbed Particle in a Box TDSE:

So far, all our calculations were based on a perfect 1-D infinite square potential well. Here, we will analyze the dynamics of a PIB system for an electron when we add a small (finite height and width) barrier in the middle of the potential well. We start with the probability distribution as a Gaussian function of the form $e^{-a(x-b)^2}$, where $a$ and $b$ are both constant that determine the width and the center of the curve, respectively. We add an initial momentum to the particle by multiplying its initial wavefunction by $e^{\gamma ix}$ where $\gamma$ is a constant that determines the strength of the initial momentum. In Matlab, this can be done using the following code


```Matlab
Psi_X=exp(-a*(x'-b).^2).*exp(c*x'*i);

```
The behavior of the particle is shown in the video bellow

<p align="center"> <img src="https://user-images.githubusercontent.com/35305574/36706076-338a610a-1b36-11e8-8ae3-6a15358414b3.gif" width="800"> </p>

The wavepacket travels towards the finite barrier then a part of the packet tunnels through the barrier, while some other part is reflected back. The ratio between the transmitted and the reflected parts of the wavepacket is mainly determined by the width and height of the barrier and also the mass of the particle.

The method I used so far in calculating the wavefunction was to directly evaluate the eigenvalues and eigenvectors of the Hamiltonian and then finding the time dependent wavefunction at the desired time ($t$) using the formula 
$$\Psi(x,t)_n=\psi(x)_n e^{\frac{-iE_n}{h}t}$$.




[Go back to home page](/README.md)
