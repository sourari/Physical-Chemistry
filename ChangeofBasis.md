{% include mathjax.html %}

## Change of basis:

There are some subtle yet very fundamental concepts in quantum mechanics that, we as students, tend to overlook when we first learn quantum mechanics. The concept of changing the basis for the Hamiltonian and eigenvectors is probably the epitome of these overlooked concepts. When solving a quantum system it is easy to be overwhelmed by the math we are solving and forget what basis we are working on. 
This page is designed to show the importance of paying attention to the basis we are working on and how to change between bases to simplify the math of solving quantum problems as well as extracting the needed information from the quantum system. In this work, we will be using examples from the paticle in a box system (see PIB), but our derivations can be applied to any quantum system.

We know that an energy eigenvector in the position space $(\psi_n)_x$ can be represented as a linear combination of the orthonormal basis vectors ${\vec{x_1},\vec{x_2},\vec{x_3}...}$ as: $(\psi_n)_x=c_1\vec{x_1}+c_2\vec{x_2}+c_3\vec{x_3}+...$.
The main idea of the position basis in 1-D is that a vector $\vec{X_i}$  represents a delta function with a values of $1$ at $i$ and has a values of $0$ everywhere else. In vector form, this is represented as $\vec{X_1}={\begin{pmatrix} 1\\\ 0\\\ 0\\\ \vdots \end{pmatrix}}_x$ and $\vec{X_2}={\begin{pmatrix} 0\\\ 1\\\ 0\\\ \vdots \end{pmatrix}}_x$ etc... This can be visualized in the following figure.

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/35716147-d57ce0c8-07a4-11e8-95c0-6e951cf81814.jpg" width="500">
</p>
<p align="center"> Graphical representation of some basis vectors </p>

This allows us to write the energy eigenvector in the position space $(\psi_n)_x$ in vector form as:

<p align="center">
$(\psi_n)_x=c_1{\begin{pmatrix} 1\\\ 0\\\ 0\\\ \vdots \end{pmatrix}}_x+c_2{\begin{pmatrix} 0\\\ 1\\\ 0\\\ \vdots \end{pmatrix}}_x+c_3{\begin{pmatrix} 0\\\ 0\\\ 1\\\ \vdots \end{pmatrix}}_x...={\begin{pmatrix} c_1\\\ 0\\\ 0\\\ \vdots \end{pmatrix}}_x+{\begin{pmatrix} 0\\\ c_2\\\ 0\\\ \vdots \end{pmatrix}}_x+{\begin{pmatrix} 0\\\ 0\\\ c_3\\\ \vdots \end{pmatrix}}_x...$
</p>

we can visualize this by plotting any of the eigenvectors, for example the ground state $(\psi_1)_x$, and the basis vectors on the same graph. This is shown in the figure bellow, where we discretized space to 10 distinct points. The intersect of the eigenvector and each of the basis vectors $\vec{x_i}$ represents the coefficient $c_i$.

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/35780329-9942a2b4-09a7-11e8-97b1-aeb6267c8684.jpg" width="500">
</p>
<p align="center"> Energy eigenvectors in position basis </p>

In general, if we want to find the energy eigenvectors in the position basis, we can use the Matlab commend [Vecs, Vals] = eig( $H_x$ ). This will solve the time-independent Schrodinger equation in position basis. 
Vecs will be a matrix with the eigenvectors (in position basis) as its columns and Vals will be a matrix with the eigenvalues on its diagonal:

Vecs = $\begin{pmatrix}
{\begin{bmatrix} \psi_1 \end{bmatrix}}_x &
{\begin{bmatrix} \psi_1 \end{bmatrix}}_x &
{\begin{bmatrix} \psi_1 \end{bmatrix}}_x &
\cdots
\end{pmatrix}$.

And Vals = $\begin{pmatrix}
E_1& 0 &0&0\\\
0& E_2&0&0\\\
0&0&E_3&0\\\ 
0&0&0&\ddots
\end{pmatrix}$.

### Hamilonian in Energy Basis:

Notice that Vals is exactly the Hamiltonian in the energy basis, $H_E$. To visualize that it is indeed $ H_E $, we write the TISE in the energy basis as follow:
$H_E {(\psi_n)}_E = E_n {(\psi_n)}_E $, which can be rewritten in matrix form (we will only show it for 3x3 matrix for simplicity, the math would be the same for any nxn matrix) as:

<p align="center"> $ \begin{pmatrix}
E_{11}& E_{12} &E_{13}\\\
E_{21}& E_{22} &E_{23}\\\
E_{31}& E_{32} &E_{33}
\end{pmatrix} {\begin{pmatrix} x\\\ y\\\ z \end{pmatrix}}_E = E_n {\begin{pmatrix} x\\\ y\\\ z \end{pmatrix}}_E $. </p>

So,
<p align="center"> $\begin{pmatrix}
x E_{11}+ y E_{12} +z E_{13}\\\
x E_{21}+ y E_{22} +z E_{23}\\\
x E_{31}+ y E_{32} +z E_{33}
\end{pmatrix} = E_n {\begin{pmatrix} x\\\ y\\\ z \end{pmatrix}}_E$. </p>

Applying the above equation for ${(\psi_1)}_E = {\begin{pmatrix} 1\\\ 0\\\ 0 \end{pmatrix}}_E $, ${(\psi_2)}_E = {\begin{pmatrix} 0\\\ 1\\\ 0 \end{pmatrix}}_E $ and ${(\psi_3)}_E = {\begin{pmatrix} 0\\\ 0\\\ 1 \end{pmatrix}}_E $. 
We can easily see that all the off-diagonal terms will go to zero and we are left with:

<p align="center"> $H_E=  \begin{pmatrix}
E_1& 0 &0\\\
0& E_2&0\\\
0&0&E_3
\end{pmatrix}$= Vals. </p>

### Change of Basis:

Using our Vecs matrix we can go from energy eigenvectors in energy basis ${\psi_n}_E$ to energy eigenvectors in position basis ${\psi_n}_x$. This can be achieved as follow:
If we "operate" the Vecs matrix on ${\psi_1}_E$ we have:
$\begin{pmatrix}
{\begin{bmatrix} \psi_1 \end{bmatrix}}_x &
{\begin{bmatrix} \psi_1 \end{bmatrix}}_x &
{\begin{bmatrix} \psi_1 \end{bmatrix}}_x &
\cdots
\end{pmatrix} {\begin{pmatrix} 1\\\ 0\\\ 0 \end{pmatrix}}_E = {\begin{bmatrix} \psi_1 \end{bmatrix}}_x $. So we obtained the first eigenvector in position basis. We can use this method for any ${\psi_n}_x$ by operating the Vecs matrix on the corresponding ${\psi_n}_E$. 




