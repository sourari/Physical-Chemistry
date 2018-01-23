{% include mathjax.html %}

#  Key Quantum Ideas

## $1)$ Quantum Mechanics Using Linear Algebra
Taking a basis formed by linearly independent vectors $|1>, |2>, |3>... |n>$ in n-dimensional space, we can write any vector in this space as a linear combination of these vectors.\\
We can then write a state vector $|v>$ as $$|v>=v_1\begin{bmatrix} 1 \\\ 0 \\\ \vdots \\\ 0 \end{bmatrix}+v_2\begin{bmatrix} 0 \\\ 1 \\\ \vdots \\\ 0 \end{bmatrix}+v_n\begin{bmatrix} 0 \\\ 0 \\\ \vdots \\\ 1 \end{bmatrix}=\begin{bmatrix} v_{1} \\\ v_{2} \\\ \vdots \\\ v_{n} \end{bmatrix}$$ and another vector $|w>=w_1\begin{bmatrix} 1 \\\ 0 \\\ \vdots \\\ 0 \end{bmatrix}+w_2\begin{bmatrix} 0 \\\ 1 \\\ \vdots \\\ 0 \end{bmatrix}+w_n\begin{bmatrix} 0 \\\ 0 \\\ \vdots \\\ 1 \end{bmatrix}=\begin{bmatrix} w_{1} \\\ w_{2} \\\ \vdots \\\ w_{n} \end{bmatrix}$.\\
We can also write $|v>$ and $|w>$ in a more formal and concise way as\\
$$|v>= \sum_{n=1}^{n}v_i |i> \ and \ |w>= \sum_{n=1}^{n}w_i |i> $$

### 1.1 Inner Product
The inner product of $|v>$ and $|w>$ is defined as
$$<v,w>=\sum_{n=1}^{n}v_i ^*w_i={\begin{bmatrix} v_{1} & v_{2} & ... & v_{n} \end{bmatrix}}^* \begin{bmatrix} w_{1} \\\ w_{2} \\\ \vdots \\\ w_{n} \end{bmatrix}$$

In quantum mechanics, the basis vectors In quantum mechanics, the basis vectors $|1>, |2>... |n>$ represent the eigenvectors of a quantum operator such as the Hamiltonian $\hat{H}$ or the momentum operator $\hat{P}$. These vectors are orthonormal, meaning that they are unit vectors and are mutually orthogonal. This can be summarized as follow:
$$<i,j>=\begin{cases} 1 \ for \ i=j \\ 0 \ for \ i\neq j \end{cases} = \delta_{ij}$$
