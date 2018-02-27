{% include mathjax.html %}


## Perturbed Particle in a Box TDSE:

So far, all our calculations were based on a perfect 1-D infinit square potential well. Here, we will analyse the behavior of an electron in a PIB when we add a small (finite hight and width) barrier in the middle of the potential well. We start with the probability distribution as a gaussian function of the form $e^{-a(x-b)^2}$, where $a$ and $b$ are both constant that determine the width and the center of the curve, respectively. We add an initial momentum to the particle by multiplying its initial wavefunction by $e^{\gamma ix}$ where $\gamma$ is a constant that determines the strength of the initial momentum. I Matlab, this can be added by the following code

```Matlab
Psi_X=exp(-a*(x'-b).^2).*exp(c*x'*i);

```
We obtain:

<p align="center"> <img src="https://user-images.githubusercontent.com/35305574/36706076-338a610a-1b36-11e8-8ae3-6a15358414b3.gif" width="800"> </p>




