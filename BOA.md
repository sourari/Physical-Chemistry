{% include mathjax.html %}

# Born-Oppenheimer Approximation ($H_2^+$)

So far in my analysis of quantum systems I have only considered systems with one particle or at most two particles (in the case of electric dipoles). In this page, I will take huge step and try a system of 3 particle. A naïve who is not familiar with quantum mechanics would think if we can solve a simple two-body system then we can scale our methods to any number of particle. Sadly, nature is not that nice and it turns out that three-body problems (or many-body problems in general) in quantum mechanics are unsolvable analytically, and we have to resort to approximation technique to study these systems.   

For example, consider $H_2^+$ shown in Fig.1 bellow. It is composed of three particles: 2 protons and 1 electrons. The Hamiltonian of the system is given by the sum of the kinetic energy and potential energy of each particle.

<p align="center"><img src="https://user-images.githubusercontent.com/35305574/38473469-79e4be14-3b5e-11e8-8c9e-887bc297ffff.jpg" width="500"></p>
<p align="center">Fig.1 (sparknote)</p>

We can write the Hamiltonian as:

$\hat{H}=\frac{-\hbar^2 }{2M_a}\nabla^2_a + \frac{-\hbar^2 }{2M_b}\nabla^2_b + \frac{-\hbar^2 }{2M_e}\nabla^2_e + \frac{-q^2}{4\pi \epsilon_0 r_a} + \frac{-q^2}{4\pi \epsilon_0 r_b}+ \frac{q^2}{4\pi \epsilon_0 R_ab}$



[Go back to home page](/README.md)


