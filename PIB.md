{% include mathjax.html %}


# Particle in a Box

The first quantum system we will explore is the particle in a box (PIB) system. 
We restrict our study to a single particle (an electron) in a 1-dimentional box of width a=5nm.
The potential energy inside the box is set to 0. At the boundary, we set the potential energy to a value that we know will be higher than the particle’s total energy, but also small enough to make the computation work.
The potential energy (presented in Figure2.1) is then given by:

<p align="center"> $V=\begin{cases} 0, & \mbox{if } 0<x<a \\\ 10^{-5}j, & \mbox{otherwise} \end{cases}$ </p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/35600148-72b520aa-05fa-11e8-88bf-b6bf9e10ba02.jpg" width="500">
</p>
<p align="center">Figure2.1: Potential energy</p>

The potential energy is given by a matrix in the position basis. The potential matrix has the values of the potential energy for reach position (x) along its diagonal. The number of position points is discrete and can easily be varied in our Matlab code depending on the degree of precision needed for our calculations.
To create the potential energy matrix in Matlab, we first need to create a square matrix of the desired size. The matrix originally has zeros in all its entries, then we add the potential energy values on its diagonal using the following code:

```Matlab
v=zeros(pts,1)    %creates a matriz of zeros; 
v([1:barrier_width, (end-(barrier_width-1):end)])=barht;  
V=diag(v);        %add the energy values on the diagonal entries of the potential matrix

```

The next step is to construct the kinetic energy matrix. The challenging part of this step is to create a matrix that take the second derivative of the wavefunction. We know that the first derivate of a function $f(x)$ at a point $x_0$ can be approximated as:

<p align="center"> $\frac{f(x_0+1)-f(x_0)}{\Delta x}$ or $\frac{f(x_0) - f(x_0-1)}{\Delta x}$. </p>

The two expressions give slightly different values of the derivative, the first expression is labeled right-derivative and the second one is labeled left-derivative. Knowing that the right-derivative is obtained by subtracting the value of the $x_0$ element of the function from the subsequent element, we can then guess the entries of the elements of the right-derivative matrix, $R$. 
The diagonal elements $R_{i,i}$ of the matrix must have a values of $-1$ and off diagonal elements $R_{i+1,i}$ must have a values of $1$ to create the $f(x_0+1)-f(x_0)$ operation. All other elements must be zeros. We should also not forget to multiply the matrix by $\frac{1}{\Delta x}$ to complete the right-derivation operation.
Similarly, we construct the left-derivative matrix, $L$. This time, the diagonal elements must have values of $1$, while off diagonal elements $R_{i-1,i}$ have values of $-1$.

Now the second derivative matrix can then be obtained by multiplying the left and right derivative matrices:

<p align="center"> $D=LR= \begin{bmatrix}
-2& -1 &      & 0 \\\
-1 & -2  & -1 \\\
0 &   \ddots  & \ddots & \ddots                      
\end{bmatrix}$ </p>

Therefore, the kinetic energy can be expressed in matrix form as:

<p align="center"> $T=\frac{-{\hbar}^2}{2m} \begin{bmatrix}
-2& -1 &      & 0 \\\
-1 & -2  & -1 \\\
0 &   \ddots  & \ddots & \ddots                      
\end{bmatrix}$ </p>

Now putting everything together, we can solve the TISE in Matlab and obtain the following eigenvectors: 

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/35598882-f4f224e8-05f3-11e8-893f-34fd8c86dd72.jpg" width="600">
</p>
<p align="center">Figure2.2: Wavefunctions for 3 different energy levels of the PIB system </p>
