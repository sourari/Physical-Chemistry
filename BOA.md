{% include mathjax.html %}

# Born-Oppenheimer Approximation ($H_2^+$)

So far in my analysis of quantum systems I have only considered systems with one particle or at most two particles (in the case of electric dipoles). In this page, I will take huge step and try a system of 3 particle. A naïve student who is not familiar with quantum mechanics would think that if we can solve a simple two-body system then we can scale our methods to any number of particle. Sadly, nature is not that nice and it turns out that three-body problems (or many-body problems in general) in quantum mechanics are analytically unsolvable, and we have to resort to approximation technique to study these systems.   

For example, consider $H_2^+$ shown in Fig.1 bellow. It is composed of three particles: 2 protons and 1 electrons. The Hamiltonian of the system is given by the sum of the kinetic energy and potential energy of each particle.

<p align="center"><img src="https://user-images.githubusercontent.com/35305574/38473469-79e4be14-3b5e-11e8-8c9e-887bc297ffff.jpg" width="500"></p>
<p align="center">Fig.1</p>

We can write the Hamiltonian as:

<p align="center">$\hat{H}=\hat{T}_{nuclear}+\hat{T}_{electron}+\hat{V}_{nuc-e}+\hat{V}_{nuc-nuc}$</p>

<p align="center">$=(\frac{-\hbar^2 }{2M_a}\nabla^2_a + \frac{-\hbar^2 }{2M_b}\nabla^2_b) + \frac{-\hbar^2 }{2M_e}\nabla^2_e + (\frac{-q^2}{4\pi \epsilon_0 r_a} + \frac{-q^2}{4\pi \epsilon_0 r_b})+ \frac{q^2}{4\pi \epsilon_0 R_{ab}}.$</p>

Therefore, the TISE is given by

<p align="center">$\hat{H}\Psi(r,R)=\xi \Psi(r,R)$</p>
so
<p align="center">$(\hat{T}_{nuclear}+\hat{T}_{electron}+\hat{V}_{nuc-e}+\hat{V}_{nuc-nuc})\Psi(r,R)=\xi \Psi(r,R).$</p>

To solve this TISE we need to resort once again to the separation of variables trick and let

<p align="center">$\Psi(r,R)=\psi(r;R)\chi(R),$</p>
where $\psi(r;R)$ means that $\psi$ is a function of $r$ and has $R$ as a parameter.

So the TISE becomes

<p align="center">$(\hat{T}_{nuclear}+\hat{T}_{electron}+\hat{V}_{nuc-e}+\hat{V}_{nuc-nuc})\psi(r;R)\chi(R)=\xi \psi(r;R)\chi(R),$</p>

such that

<p align="center">$\hat{T}_{nuclear}(\psi \chi)+\hat{T}_{electron}(\psi \chi)+\hat{V}_{nuc-e}(\psi \chi)+\hat{V}_{nuc-nuc}(\psi \chi)$</p>
  <p align="center">$=\xi \psi \chi.$</p>

Then dividing both sides by $\psi \chi$ we have

<p align="center">$\frac{\hat{T}_{nuclear}(\psi \chi)}{\psi \chi}+ \frac{\hat{T}_{electron}\psi}{\psi}+ \hat{V}_{nuc-e} +\hat{V}_{nuc-nuc} =\xi.$</p>

We can see that the first term should be the most challenging to deal with, so let’s start with it. We have 

<p align="center"> $\hat{T}_{nuclear}(\psi \chi)= (\frac{-\hbar^2 }{2M_a}\nabla^2_a + \frac{-\hbar^2 }{2M_b}\nabla^2_b) (\psi \chi) .$</p>

<p align="center"> $= \frac{-\hbar^2 }{2M_a}\nabla^2_a(\psi \chi) + \frac{-\hbar^2 }{2M_b}\nabla^2_b(\psi \chi) .$</p>

The two terms in the equation above are similar, so we can solve the first term and determine the second one by analogy.


<p align="center"> $\frac{-\hbar^2 }{2M_a}\nabla^2_a(\psi \chi) = \frac{-\hbar^2 }{2M_a} \frac{\partial}{\partial R_a} (\frac{\chi \partial \psi}{\partial R_a} + \frac{\psi \partial \chi}{\partial R_a}) $</p>

<p align="center"> $= \frac{-\hbar^2 }{2M_a}[(\chi \frac{\partial^2 \psi}{\partial {R_a}^2}+\frac{\partial \psi}{\partial {R_a}}\frac{\partial \chi}{\partial {R_a}}) +  (\psi \frac{\partial^2 \chi}{\partial {R_a}^2}+\frac{\partial \psi}{\partial {R_a}}\frac{\partial \chi}{\partial {R_a}})] $</p>

Now comes the Born-Oppenheimer approximation. We know that the mass of the proton is 1836 times greater than that of the electron. Therefore, as the whole system (electron + two protons) move in space, the electron also moves relative to the center of mass of the system. We can then approximate that the rate of change of $\psi$ with respect to $R_a$ is insignificant. So that

<p align="center"> $\frac{\partial^2 \psi}{\partial {R_a}^2}= \frac{\partial \psi}{\partial {R_a}}=0 $.</p>

We then obtain

<p align="center"> $\frac{-\hbar^2 }{2M_a}\nabla^2_a(\psi \chi) = \frac{-\hbar^2 }{2M_a}\psi \frac{\partial^2 \chi}{\partial {R_a}^2} $.</p>

By analogy we also have 

<p align="center"> $\frac{-\hbar^2 }{2M_b}\nabla^2_b(\psi \chi) = \frac{-\hbar^2 }{2M_b}\psi \frac{\partial^2 \chi}{\partial {R_b}^2}$. $</p>

Therefore, the TISE become

<p align="center"> $\frac{\frac{-\hbar^2 }{2M_a} \frac{\partial^2 \chi}{\partial {R_a}^2}}{\chi} + \frac{\frac{-\hbar^2 }{2M_b} \frac{\partial^2 \chi}{\partial {R_b}^2}}{\chi} + \frac{\hat{T}_{electron} \psi}{\psi} + \hat{V}_{nuc-e}+\hat{V}_{nuc-nuc} =\xi$.</p>

The TISE can be rewritten as 

<p align="center"> $(\frac{\hat{T}_{nuclear} \chi}{\chi} + \frac{\chi}{\chi} \hat{V}_{nuc-nuc})+ (\frac{\hat{T}_{electron} \psi}{\psi} + \frac{\psi}{\psi} \hat{V}_{nuc-e})=\xi$.</p>

Call the second term $E_e$ and factor out the $\chi$ in the first term to obtain

<p align="center"> $(\frac{\hat{T}_{nuclear}}{\chi} + \frac{1}{\chi} \hat{V}_{nuc-nuc})\chi+ E_e=\xi$.</p>

Then multiply both sides by $\chi$ to obtain

<p align="center"> $(\hat{T}_{nuclear} + \hat{V}_{nuc-nuc})\chi + E_e \chi =\xi \chi$.</p>

This can be rewritten as 

<p align="center"> $\hat{T}_{nuclear} \chi + (\hat{V}_{nuc-nuc}+E_e) \chi =\xi \chi$.</p>

Call the terms in parenthesis $ \hat{V}_{nuclear}$ to obtain

<p align="center"> $\hat{T}_{nuclear} \chi + \hat{V}_{nuclear} \chi =\xi \chi$.</p>

This gives as an equation for the dynamics of the two protons. The potential energy operator $\hat{V}_{nuclear}$ is a combination of the nucleus-nucleus repulsion and the electron-nucleus attraction. For large separation between the two nuclei the dominant interaction is the electron-nucleus. On the other hand, for small separation between the nuclei, the nucleus-nucleus repulsion is the dominant interaction. Therefore, the potential energy will have the form shown in Fig.2 bellow.


<p align="center"><img src="https://user-images.githubusercontent.com/35305574/38476034-bac110fc-3b79-11e8-8f23-d9108b18a1d9.jpeg" width="500"></p>
<p align="center">Fig.2</p>

The figure above gives as the energy of the electron when it is in the two-nuclei system for each separation between the two nuclei. We can use this model to study the interactions between three atoms such as the exchange reaction
<p align="center"> A + B-C $\rightarrow$ A-B + C</p>

This will be the focus of the [next page](/dynamics.md).



[Go back to home page](/README.md)

