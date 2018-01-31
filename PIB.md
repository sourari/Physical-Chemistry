{% include mathjax.html %}

# Particle in a Box

The first quantum system we explore is the particle in a box (PIB) system. 
We restrict our study to a single particle (an electron) in a 1-dimentional box of width a=5nm.
The potential energy inside the box is set to 0. At the boundary, we set the potential energy to a value that we know will be higher than the particle’s total energy, but also small enough to make the computation work.
The potential energy (presented in Figure2.1) is then given by:

$V=\begin{cases} 0, & \mbox{if } 0<x<a \\\ 10^{-5}j, & \mbox{otherwise} \end{cases}$

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/35600148-72b520aa-05fa-11e8-88bf-b6bf9e10ba02.jpg" width="500">
</p>
<p align="center">Figure2.1: Potential energy</p>

The potential energy is given by a matrix in the position basis. The potential matrix has the values of the potential energy for reach position (x) along its diagonal. The number of position points is discrete and we can vary it easily in our Matlab code depending the degree of precision we need in our calculation of eigenvectors.
To create the potential energy matrix in Matlab we first need to create a square matrix of the desired size. The matrix originally has zeros in all its entries then we add the potential energy values of its diagonal using the following code:

v=zeros(pts,1); 
v([1:barrier_width, (end-(barrier_width-1):end)])=barht;
V=diag(v);  

The next step is to construct the potential energy matrix. The challenging part of this step is to create a matrix that take the second derivative of the wavefunction. We know that the first derivate of a function $f(x)$ at a point $x_0$ can be approximated as:\\
<p align="center"> $\frac{f(x_0+1)-f(x_0)}{\Delta x}$ or $\frac{f(x_0-1)-f(x_0)}{\Delta x}$ </p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/35598882-f4f224e8-05f3-11e8-893f-34fd8c86dd72.jpg" width="600">
</p>
<p align="center">Figure2.2: Wavefunctions for 3 different energy levels of the PIB system </p>
