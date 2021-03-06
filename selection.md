{% include mathjax.html %}

# Selection Rules:

So far in my study I have explored the PIB system fairly deeply. I showed how the energy of the particle is quantized and that the energy levels are equally separated. But this study is only relevant to an isolated system with no interaction. In reality, a quantum system will continuously undergo transitions between different energy levels spontaneously and with stimulations from the environment. A question that should be asked is: are all transitions between energy levels allowed? The simple answer is no. Transitions have to obey certain rules that originate from the laws of conservation of energy and momentum (both linear and angular momentum), these rules are called the selection rules. 

What makes a quantum system transition from one energy level to another? This ties back to light-matter interactions. To understand these interactions, we have to revisit the idea of electric dipoles ([see this link](/dipoles.md)). An electric dipole can represent the electron (negative part of the dipole) and the nucleus (positive part of the dipole) of an atom or can represent a molecule. Each dipole has a natural frequency often referred to as $\omega_0$. If the frequency of an incident electromagnetic field ($\omega$) is resonant with the natural frequency of the dipole, $\omega=\omega_0$, then the light would be absorbed and this would trigger a vibration of the dipole. The further the frequency of light is from $\omega_0$ the less probable it is for light to be absorbed. Sounds like we are getting closer to some rules of transitions isn’t it?

To find the probability of a transition from a state $\psi_n$ to $\psi_m$, given $\omega 	\approx \omega_0$, we need to evaluate the transition integral given by
<p align="center"> $M_{nm}=\int \psi_n \cdot \vec{\mu} \cdot \psi_m $. </p>

As you would expect, I want to change this integral into an inner product. The transition probability is the given by
<p align="center"> $M_{nm}=<\psi_n,  \vec{\mu} \psi_m >$. </p>
  
This form is ready for Matlab computation. I used the following code to compute the transition probability.
```Matlab
M=Vecs' *diag(x)* Vecs;
```
I used the old SHO code with the above code to determine the selection rules for the SHO system. The selection rules for this system are shown in Fig.1. The horizontal axis shows the final state $m$ and the vertical axis shows the initial state $n$. From the figure, we can see that transitions only occur for $m=n \pm 1$. In other words, the transition rule is $\Delta \nu=\pm1$, following the convention that for SHO we use the quantum number $\nu$ and not $n$.


<p align="center"><img src="https://user-images.githubusercontent.com/35305574/38471395-98f4fa00-3b3e-11e8-9b67-01ad0d952ac1.jpg" width="500"></p>

The SHO model is very useful to understand the selection rules, however, to a more realistic model of molecular vibration is given by the Lennard-Jones potential. This potential is shown in the [next page](/LJP.md).




[Go back to home page](/README.md)
