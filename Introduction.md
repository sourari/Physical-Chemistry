{% include mathjax.html %}


## Introduction to Quantum Mechanics Concepts Using Linear Algebra
Taking a basis formed by linearly independent vectors $|1>, |2>, |3>... |n>$ in n-dimensional space, we can write any vector in this space as a linear combination of these vectors.\\
We can then write a state vector $|v>$ as $$|v>=v_1\begin{bmatrix} 1 \\\ 0 \\\ \vdots \\\ 0 \end{bmatrix}+v_2\begin{bmatrix} 0 \\\ 1 \\\ \vdots \\\ 0 \end{bmatrix}+v_n\begin{bmatrix} 0 \\\ 0 \\\ \vdots \\\ 1 \end{bmatrix}=\begin{bmatrix} v_{1} \\\ v_{2} \\\ \vdots \\\ v_{n} \end{bmatrix}$$ and another vector $|w>=w_1\begin{bmatrix} 1 \\\ 0 \\\ \vdots \\\ 0 \end{bmatrix}+w_2\begin{bmatrix} 0 \\\ 1 \\\ \vdots \\\ 0 \end{bmatrix}+w_n\begin{bmatrix} 0 \\\ 0 \\\ \vdots \\\ 1 \end{bmatrix}=\begin{bmatrix} w_{1} \\\ w_{2} \\\ \vdots \\\ w_{n} \end{bmatrix}$.\\
We can also write $|v>$ and $|w>$ in a more formal and concise way as
$$|v>= \sum_{n=1}^{n}v_i |i> \ and \ |w>= \sum_{n=1}^{n}w_i |i> $$

### 1.1 Inner Product
The inner product of $|v>$ and $|w>$ is defined as
$$<v,w>=\sum_{n=1}^{n}v_i ^*w_i={\begin{bmatrix} v_{1} & v_{2} & ... & v_{n} \end{bmatrix}}^* \begin{bmatrix} w_{1} \\\ w_{2} \\\ \vdots \\\ w_{n} \end{bmatrix}$$
In quantum mechanics, the basis vectors In quantum mechanics, the basis vectors $|1>, |2>... |n>$ represent the eigenvectors of a quantum operator such as the Hamiltonian $\hat{H}$ or the momentum operator $\hat{P}$. These vectors are orthonormal, meaning that they are unit vectors and are mutually orthogonal. This can be summarized as follow:\\
$$<i,j>=\begin{cases} 1 \ for \ i=j \\ 0 \ for \ i\neq j \end{cases} = \delta_{ij}$$

### 1.2 Time Independent Schroedinger Equation (TISE)
The single most important piece of quantum mechanics is the TISE defined as\\
$$\hat{H}\psi=E\psi$$, where $\psi$ is the eigenfunction of the system, $E$ is the value of the energy energy of the system and $\hat{H}=\hat{T}+\hat{V}$ is the Hamiltonian operator for a one-dimensional system. Here $\hat{T}=-\frac{\hbar^2}{2m}\frac{d^2}{dx^2}$ and $\hat{V}$ will be defined by the given quantum system studied.

### 1.2 Constructing Potential Energy Matrix
From the TISE, we know that the potential energy operator, $\hat{V}$ should be a matrix operating of the wavefunction vector $\psi$. So $\hat{V}$ should be a square matrix of size $n$, where $n$ is the number of entries in the column vector representing the wavefunction. Therefore $\hat{V}$ must be of the form\\
$\begin{bmatrix}
 v_{11} & 0 & & \cdots & & 0&  0 \\\
 0 & v_{22} & & \cdots & & 0&  0 \\\
 \vdots &  \vdots &   & \ddots  & \vdots & \vdots\\\
 0 & 0 & & \cdots & & v_{(n-1)(n-1)}&  0 \\\
0 & 0 & & \cdots & & 0&  v_{nn}
\end{bmatrix}$

Example:
Let's consider a 1-dimensional potential represented in the figure below. 
<img src="https://user-images.githubusercontent.com/35305574/35256754-4f4343e6-ffc3-11e7-9027-26fe1c8dd879.jpg" width="400">

The potential matrix for this potential is:
$\hat{V}= \begin{bmatrix}
4& 0& 0& 0& 0&0 & 0\\\
0& 0& 0& 0& 0&0 & 0\\\
0& 0& 0& 0& 0&0 & 0\\\
0& 0& 0& 3& 0&0 & 0\\\
0& 0& 0& 0& 2&0 & 0\\\
0& 0& 0& 0& 0&0 & 0\\\
0& 0& 0& 0& 0&0 & 0
\end{bmatrix}$
