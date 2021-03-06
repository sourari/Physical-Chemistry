{% include mathjax.html %}

# Molecular Dynamics:

This is my final page and it will build on the knowledge accumulated through my whole project to study some simplified molecular dynamics. Consider three atoms A, B and C. For simplicity, let’s assume they are confined to only move in one direction, call it x-direction. Let’s assume the system starts with a molecule B-C and a separate atom A. The atom A approaches the molecule with some velocity $v$, the question I want to answer is A break the bond of B-C and for a molecule with either B or C? What are the requirements for such bond breaking/forming to occur? 

Each pair of the three particles will have a potential energy that looks like the Fig.2 of the previous page. So, we can express the potential of the system as a surface in function of the distances $r_{BC}$ and $r_{AB}$ (we do not need to worry about $r_{AC}$ since the atoms are on a line such that $r_{AC}$=$r_{AB}$+$r_{BC}$). The surface is shown in Fig.1 and Fig.2 bellow for an early and a late barrier, respectively.

<p align="center"><img src="https://user-images.githubusercontent.com/35305574/38695528-862533d0-3e5a-11e8-95ce-018301e0b91d.jpg" width="500"></p>
<p align="center">Fig.1</p>

<p align="center"><img src="https://user-images.githubusercontent.com/35305574/38695530-87e11e1e-3e5a-11e8-9136-6b143f23df3b.jpg" width="500"></p>
<p align="center">Fig.2</p>

In the figures above the vertical axis represents the potential energy and the two horizontal axes represent the distance $r_{AB}$ and $r_{BC}$. The early barrier represents an exothermic reaction with the products having lower energy that the reactants. The late barrier represents an endothermic reaction with the products having higher energy that the reactants.

Now let’s run a simulation that will show as how the system behaves as atom A approaches the molecule B-C. Let’s start with an early barrier. Fig.3 bellow shows the relative positions of the three atoms as well as the evolution of the energy of the system. I start the system with a high velocity for the atom A moving towards the molecule B-C.

![Four3](/ep.gif) 
<p align="center">Fig.3</p>

We see that the molecule B-C initially vibrates at its natural frequency, then as the atom A gets closer it perturbs the system and ends up breaking B-C and forming a new molecule A-B. This reaction is an exothermic reaction and is given by the exchange reaction

<p align="center"> A + B-C $\rightarrow$ A-B + C</p>
The figure also shows how the energy of the system evolves. Notice a saddle point in the energy surface where the transition from B-C to A-B occurs. Whether the exchange reaction
Will occur or not depends on whether or not the system has enough energy to cross the saddle point. 

Now if we decrease the initial velocity of atom A, the reaction does not occur as shown in the animation of Fig.4.

![Four3](/eno.gif) 
<p align="center">Fig.4</p>

Now for a late barrier, the saddle point is shifted to the left and we need more kinetic energy in atom A for the reaction to occur. The figures bellow show the example of a reaction and an example of a system that did not have enough energy to break the B-C bond.  

<p align="center"><img src="https://user-images.githubusercontent.com/35305574/38706575-aba155a0-3e7b-11e8-851b-5e114937c54a.png" width="500"></p>
<p align="center">Fig.5</p>

<p align="center"><img src="https://user-images.githubusercontent.com/35305574/38706576-ad0f0914-3e7b-11e8-8b6d-082edac35a08.png" width="500"></p>
<p align="center">Fig.6</p>

The examples above are based on the Morse potential, so how about the Lennard-Jones (L-J) potential? Recall the shape of the L-J potential we saw before, it has a much deeper well than the Morse potential. Therefore, we should expect to see a lower probability for the reaction taking place than what we observed above. Fig.7 bellow shows the potential energy surface for L-J. The L-J potential can be used to model the interaction between nobel gases.

<p align="center"><img src="https://user-images.githubusercontent.com/35305574/38707059-b6ac0448-3e7d-11e8-8847-c75989ce6ef5.png" width="500"></p>
<p align="center">Fig.7</p>




[Go back to home page](/README.md)
