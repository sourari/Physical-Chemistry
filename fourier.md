{% include mathjax.html %}

# Fourier Transform:
So far in my analysis of quantum systems, I have been mainly using the position basis. However, there are a lot of information that are hidden in other bases such as the momentum basis. Luckily, there is a powerful mathematical tool that can help us navigate easily between position and momentum bases. This mathematical tool is of course the glorious Fourier Transform. In this page, I will be introducing the basic math behind the Fourier transform and how it is helpful in physical chemistry.

The Fourier Transform decomposes a function into the sum of complex exponential function. These functions have different frequencies and form a basis. The idea on Fourier Transform is to express our original function in this new basis (a familiar approach to that we discussed [here](/ChangeofBasis.md)).

Let’s explore the example of transforming a function from position space to momentum space. In momentum space, we use the wavenumber $k=\frac{2\pi}{\lambda}$ as our variable. To see why we use $k$ for the momentum space let’s apply the momentum operator on an arbitrary function $f(x)=e^{ikx}$. We obtain

<p align="center"> $\hat{P}e^{ikx}= -i \hbar \frac{\partial}{\partial x}e^{ikx}$. </p>
so 
<p align="center"> $\hat{P}e^{ikx}= k \hbar e^{ikx}$. </p>
Therefore, the momentum is the wavenumber $k$ multiplied by $\hbar$.

Here, I want to show how the Fourier Transform take as an input as function in position space $f(x)$ and gives us a new function in $k$-space $\hat{f}(k)$. As we defined above, the Fourier Transform specifies how much a complex exponential function $e^{ikx}$ with wavenumber $k$ contributes to the function $f(x)$.  As we would expect, each $e^{ikx}$ will contribute to $f(x)$ by a coefficient that is dependent on the value of $k$. We define this coefficient by $\hat{f}(k)$. The function $f(x)$ is, therefore, the sum of all these contributions and can be written as
<p align="center"> $f(x)=\sum_{k} \hat{f}(k) e^{ikx}$. </p>

The expression above is for a finite sum for discrete values of $k$. To express $f(x)$ in function of continuous and infinite values of $k$, we have to change the sum into an integral to obtain

<p align="center"> $f(x)=\frac{1}{\sqrt[]{2\pi}}\int_{-\infty}^{\infty} \hat{f}(k) e^{ikx}dk$. </p>

The above equation is known as the inverse Fourier Transform. The Fourier Transform is then given by
<p align="center"> $\hat{f}(k)=\frac{1}{\sqrt[]{2\pi}}\int_{-\infty}^{\infty} f(x) e^{-ikx}dx$. </p>






<p align="center"> $H \Psi(x,t)= i \hbar \frac{\partial}{\partial t} \Psi(x,t) dx$, </p>



[Go back to home page](/README.md)
