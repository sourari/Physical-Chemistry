{% include mathjax.html %}

## Change of basis:

There are some subtle yet very fundamental concepts in quantum mechanics that, we as students, tend to overlook when we first learn quantum mechanics. The concept of changing the basis for the Hamiltonian and eigenvectors is probably the epitome of these overlooked concepts. When solving a quantum system It is to be overwhelmed by the math we are solving and forget what basis we are working on. 
This page is designed to show the importance of paying attention to the basis we are working on and how to change between bases to simplify the math of solving quantum problems as well as extracting the needed information from the quantum system. Our work will be using examples from the paticle in a box system, but our derivations can be applied to any quantum system.

We know that an energy eigenvector in the position space $\psi_n(x)$ can be represented as a linear combination of the orthonormal basis vectors ${\vec{x_1},\vec{x_2},\vec{x_3}...}$ as: $\psi_n(x)=c_1\vec{x_1}+c_2\vec{x_2}+c_3\vec{x_3}+...$.
The main idea of the position basis in 1-D is that a vector $\vec{X_i}$  represents a delta function with a values of $1$ at $i$ and has a values of $0$ everywhere else. In vector form, this is represented as $\vec{X_1}=\begin{pmatrix} 1\\\ 0\\\ 0\\\ \vdots \end{pmatrix}$ and $\vec{X_2}=\begin{pmatrix} 0\\\ 1\\\ 0\\\ \vdots \end{pmatrix}$ etc...
