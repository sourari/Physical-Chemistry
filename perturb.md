{% include mathjax.html %}

# Perturbation Theory: a Very Brief Introduction


Perturbation theory is a powerful mathematical tool that allows us to approximate and study quantum systems that we could not solve using direct calculations. The number of quantum systems that can be solved analytically are very few and they are mainly hypothetical, over simplified systems. For this reason, scientists have developed the perturbation theory, which consists of solving a complex problem by considering a simplified system (which we can compute the solution analytically) and treat the complex parts as perturbation to your simple problem. This method has been proven successful in explaining a myriad of phenomena, from the subatomic interactions to chemical bond. In this page, I will focus on the example of atomic orbitals to show some basics of how perturbation theory is useful.

Let’s consider a PIB system with a barrier in the middle of the potential well. Consider the barrier to be of finite height and width as shown in Fig.1 bellow.
<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38461524-b969859c-3aa0-11e8-85d4-cf257f26b9cc.jpg" width="500">
</p>
<p align="center">Fig.1</p>

In this case we can compute the wavefunction of the left well and the right well separately. Then we can use the wavefunction of the two wells as a basis for the total wavefunction. This can be mathematically expressed as $\psi_{tot} \approx c_{left} \psi_{left}+ c_{right} \psi_{right} $.

The wavefunctions of the separate wells are shown in Fig.2. The figure shows three eigenstates for $n=1$, $n=2$ and $n=3$ (from lowest to highest in the figure).  

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38461733-faea5e2e-3aa5-11e8-8949-ef3102b6ea2f.jpg" width="500">
</p>
<p align="center">Fig.2</p>

Fig.2 also shows two different linear combinations (for each value on $n$ ) of the right and left wavefunction to construct the total wavefunction. These linear combinations are shown in Fig.3 bellow. The blue rectangles represent the coefficient of the left wavefunction ($c_{left}$) and the yellow rectangles represent the coefficient of the right wavefunction ($c_{right}$). 

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38461826-2268d834-3aa8-11e8-9d2e-3c0b86c882f6.jpg" width="500">
</p>
<p align="center">Fig.3</p>

We see that when both $C_{left}$ and $C_{right}$ are positive the total energy of the system is higher than when $C_{left}$ is negative and $C_{right}$ is positive, this is shown in the offset of the total wavefunctions in Fig.2. Recall that a system with lower energy is more stable than a system with higher energy. This shows that the linear combinations with $C_{left}<0$ and $C_{left}>0$ are most stable and thinking about chemical bonding the represent a bond, while  $C_{left}>0$ and $C_{left}>0$ represents an antibond. 
The last two graphs of Fig.3 can be used to represent the bonding and antibonding (last and second to last graphs, respectively) of two 1s orbitals as shown in Fig.4. The figure shows how the electric field compresses and stretches the dipole. This is expected since when the electric field is positive it attracts the positive charge upward and pushes the negative charge downward, resulting in a stretched dipole. When the electric field is negative it pushes the positive charge downward and attracts the negative charge upwards, resulting in a compressed dipole. This results in an oscillation of the electric dipole moment.

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38461976-02621902-3aac-11e8-8150-fca251b7a6e7.gif" width="300">
</p>
<p align="center">Fig.4 (sparknote)</p>


[Go back to home page](/README.md)
