{% include mathjax.html %}

#  Key Quantum Ideas

## $1)$ Quantum Mechanics Using Linear Algebra
Taking a basis formed by linearly independent vectors $|1>, |2>, |3>... |n>$ in n-dimensional space, we can write any vector in this space as a linear combination of these vectors.\\
We can then write a state vector $|v>$ as $$|v>=v_1\begin{bmatrix} 1 \\\ 0 \\\ \vdots \\\ 0 \end{bmatrix}+v_2\begin{bmatrix} 0 \\\ 1 \\\ \vdots \\\ 0 \end{bmatrix}+v_n\begin{bmatrix} 0 \\\ 0 \\\ \vdots \\\ 1 \end{bmatrix}=\begin{bmatrix} v_{1} \\\ v_{2} \\\ \vdots \\\ v_{n} \end{bmatrix}$$ and another vector $|w>=w_1\begin{bmatrix} 1 \\\ 0 \\\ \vdots \\\ 0 \end{bmatrix}+w_2\begin{bmatrix} 0 \\\ 1 \\\ \vdots \\\ 0 \end{bmatrix}+w_n\begin{bmatrix} 0 \\\ 0 \\\ \vdots \\\ 1 \end{bmatrix}=\begin{bmatrix} w_{1} \\\ w_{2} \\\ \vdots \\\ w_{n} \end{bmatrix}$.\\
We can also write $|v>$ and $|w>$ in a more formal and concise way as\\
$|v>= \sum_{n=1}^{n}v_i |i>$ and $|w>= \sum_{n=1}^{n}w_i |i> $$\
