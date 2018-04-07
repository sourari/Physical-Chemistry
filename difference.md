{% include mathjax.html %}


## Difference Method of Evaluating the TDSE

The difference method is a powerful tool of evaluating the TDSE, or any other differential equation. The benefit of this method is that it allows us to omit the need to evaluate the differential equation (or here the Schrödinger equation) for each time, instead it builds the state at each time () from the previous state (). Therefore, this method saves us a lot of computational power and simplifies the calculation significantly. However, these benefits come with a price. Building each state from the previous, means that each calculation will build on the error of the previous calculation, hence the error will exponentially increase. 




```Matlab
Psi_X=exp(-a*(x'-b).^2).*exp(c*x'*i);

```
The behavior of the particle is shown in the video bellow

<p align="center"> <img src="https://user-images.githubusercontent.com/35305574/36706076-338a610a-1b36-11e8-8ae3-6a15358414b3.gif" width="800"> </p>

The wavepacket travels towards the finite barrier then a part of the packet tunnels through the barrier, while some other part is reflected back. The ratio between the transmitted and the reflected parts of the wavepacket is mainly determined by the width and height of the barrier and also the mass of the particle.

The method I used so far in calculating the wavefunction was to directly evaluate the eigenvalues and eigenvectors of the Hamiltonian and then finding the time dependent wavefunction at the desired time ($t$) using the formula 
$$\Psi(x,t)_n=\psi(x)_n e^{\frac{-iE_n}{h}t}$$.
This method is great and quick when we want to evaluate the wavefunction of the system. However, this method might not be as effective if we want to solve more complicated systems, such as 2-D or 3-D PIB systems. Therefore, in the [next page](/difference.md) I will introduce another method of evaluating the time-dependent wavefunctions.





[Go back to home page](/README.md)
