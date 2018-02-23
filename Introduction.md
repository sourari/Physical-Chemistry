{% include mathjax.html %}


## Introduction to Quantum Mechanics Concepts Using Linear Algebra
Linear algebra is the natural language of quantum mechanics. So it is important to begin our explorations by a quick refresher of the main ideas of linear algebra that are most relevant to quantum theory.
Linear algebra allows us to express quantum states in vector forms. This, in my opinion, makes the ideas of orthogonality and normalization of wavefunctions more intuitive. We all know, from introductory linear algebra, what it means to normalize a vector and what orthogonal sets of vectors mean. This makes our lives much easier later in our explorations.

### 1.1 Orthonormal basis
Consider a basis formed by the linearly independent vectors $|1>, |2>, |3>...|n>$ in an n-dimensional space, we can write any vector in this space as a linear combination of these vectors.
For example, we can write an arbitrary vector $|v>$ as 

<p align="center"> $|v>=v_1\begin{bmatrix} 1 \\\ 0 \\\ \vdots \\\ 0 \end{bmatrix}+v_2\begin{bmatrix} 0 \\\ 1 \\\ \vdots \\\ 0 \end{bmatrix}+v_n\begin{bmatrix} 0 \\\ 0 \\\ \vdots \\\ 1 \end{bmatrix}=\begin{bmatrix} v_{1} \\\ v_{2} \\\ \vdots \\\ v_{n} \end{bmatrix}$. </p>
and another vector $|w>$ as

<p align="center"> $|w>=w_1\begin{bmatrix} 1 \\\ 0 \\\ \vdots \\\ 0 \end{bmatrix}+w_2\begin{bmatrix} 0 \\\ 1 \\\ \vdots \\\ 0 \end{bmatrix}+w_n\begin{bmatrix} 0 \\\ 0 \\\ \vdots \\\ 1 \end{bmatrix}=\begin{bmatrix} w_{1} \\\ w_{2} \\\ \vdots \\\ w_{n} \end{bmatrix}$. </p>
We can also write $|v>$ and $|w>$ in a more formal and concise way as
 <p align="center">$|v>= \sum_{n=1}^{n}v_i |i> \ and \ |w>= \sum_{n=1}^{n}w_i |i> $. </p>

### 1.2 Inner Product
The inner product of $|v>$ and $|w>$ is defined as
<p align="center"> $<v,w>=\sum_{n=1}^{n}v_i ^*w_i={\begin{bmatrix} v_{1} & v_{2} & ... & v_{n} \end{bmatrix}} \begin{bmatrix} w_{1} \\\ w_{2} \\\ \vdots \\\ w_{n} \end{bmatrix}$.</p>
In quantum mechanics, the basis vectors $|1>, |2>... |n>$ represent the eigenvectors of a quantum operator such as the Hamiltonian $\hat{H}$ or the momentum operator $\hat{P}$. These vectors are orthonormal, meaning that they are unit vectors and are mutually orthogonal. This can be summarized as follow:
<p align="center"> $<i,j>=\begin{cases} 1 \ for \ i=j \\ 0 \ for \ i\neq j \end{cases} = \delta_{ij}$ </p>

### 1.2 Time Independent Schroedinger Equation (TISE)
The single most important piece of quantum mechanics is the TISE defined as:

<p align="center"> $\hat{H}\psi=E\psi$, </p>
where $\psi$ is the eigenfunction of the system, $E$ is the value of the energy of the system and $\hat{H}=\hat{T}+\hat{V}$ is the Hamiltonian operator. $\hat{T}=-\frac{\hbar^2}{2m}\frac{d^2}{dx^2}$ for a on-dimentional system and $\hat{V}$ will be described by the particular quantum system studied.

### 1.2 Constructing Potential Energy Matrix
From the TISE, we know that the potential energy operator, $\hat{V}$ should be a matrix operating on the wavefunction represented by a vector $\psi$. So $\hat{V}$ should be a square matrix of size $n$, where $n$ is the number of entries in the column vector representing the wavefunction. Therefore $\hat{V}$ must be of the form

<p align="center"> $\begin{bmatrix}
 v_{11} & 0 & & \cdots & & 0&  0 \\\
 0 & v_{22} & & \cdots & & 0&  0 \\\
 \vdots &  \vdots &  & \ddots & & \vdots & \vdots\\\
 0 & 0 & & \cdots & & v_{(n-1)(n-1)}&  0 \\\
0 & 0 & & \cdots & & 0&  v_{nn}
\end{bmatrix}$ </p>

Example:
Let's consider a 1-dimensional potential represented in the figure below. 
<p align="center"> <img src="https://user-images.githubusercontent.com/35305574/35784820-b0dd9018-09e9-11e8-8597-b341a167d9eb.jpg" width="600"> </p>

The potential matrix for this potential is:
<p align="center"> $\hat{V}= \begin{bmatrix}
4& 0& 0& 0& 0&0 & 0\\\
0& 0& 0& 0& 0&0 & 0\\\
0& 0& 0& 0& 0&0 & 0\\\
0& 0& 0& 3& 0&0 & 0\\\
0& 0& 0& 0& 2&0 & 0\\\
0& 0& 0& 0& 0&0 & 0\\\
0& 0& 0& 0& 0&0 & 0
\end{bmatrix}$ </p>
