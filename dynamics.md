{% include mathjax.html %}

# Molecular Dynamics:

This is my final page and it will build on the knowledge accumulated through my whole project to study some simplified molecular dynamics. Consider three atoms A, B and C. For simplicity, let’s assume they are confined to only move in one direction, call it x-direction. Let’s assume the system starts with a molecule B-C and a separate atom A. The atom A approaches the molecule with some velocity $v$, the question I want to answer is A break the bond of B-C and for a molecule with either B or C? What are the requirements for such bond breaking/forming to occur? 

Each pair of the three particles will have a potential energy that looks like the Fig.2 of the previous page. So, we can express the potential of the system as a surface in function of the distances $r_{BC}$ and $r_{AB}$ (we do not need to worry about $r_{AC}$ since the atoms are on a line such that $r_{AC}$=$r_{AB}$+$r_{BC}$. The surface if shown in Fig.1 and Fig.2 bellow for an early and a late barrier, respectively.

<p align="center"><img src="https://user-images.githubusercontent.com/35305574/38695528-862533d0-3e5a-11e8-95ce-018301e0b91d.jpg" width="500"></p>
<p align="center">Fig.1</p>

<p align="center"><img src="https://user-images.githubusercontent.com/35305574/38695530-87e11e1e-3e5a-11e8-9136-6b143f23df3b.jpg" width="500"></p>
<p align="center">Fig.2</p>

In the figure above the vertical axis represents the potential energy and the two horizontal axes represent the distance $r_{AB}$ and $r_{BC}$. The early barrier represents an exothermic reaction with the products having lower energy that the reactant. The late barrier represents an endothermic reaction with the products having higher energy that the reactant.

Now let’s run a simulation that will show as how the system behaves as atom A approaches the molecule B-C. Let’s start with an early barrier. Fig.3 bellow shows the relative position of the three atoms as well as the evolution of the energy of the system. I start the system with a high velocity for the atom A moving towards the molecule B-C.

![Four3](/ep.gif) 






[Go back to home page](/README.md)
