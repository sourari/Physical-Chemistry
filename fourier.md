{% include mathjax.html %}

# Fourier Transform:
So far in my analysis of quantum systems, I have been mainly using the position basis. However, there are a lot of information that are hidden in other bases such as the momentum basis. Luckily, there is a powerful mathematical tool that can help us navigate easily between position and momentum bases. This mathematical tool is of course the glorious Fourier Transform. In this page, I will be introducing the basic math behind the Fourier transform and how it is helpful in physical chemistry.

The Fourier Transform decomposes a function into the sum of complex exponential function. These functions have different frequencies and form a basis. The idea on Fourier Transform is to express our original function in this new basis (a familiar approach to that we discussed [here](/ChangeofBasis.md)).

Let’s explore the example of transforming a function from position space to momentum space. In momentum space, we use the wavenumber $k=\frac{2\pi}{\lambda}$ as our variable. To see why we use $k$ for the momentum space let’s apply the momentum operator on an arbitrary function $f(x)=e^{ikx}$. We obtain

<p align="center"> $\hat{P}e^{ikx}= -i \hbar \frac{\partial}{\partialx}e^{ikx}$. </p>
so 
<p align="center"> $\hat{P}e^{ikx}= k \hbar e^{ikx}$. </p>
Therefore, the momentum is the wavenumber $k$ multiplied by $\hbar$.










<p align="center"> $H \Psi(x,t)= i \hbar \frac{\partial}{\partial t} \Psi(x,t)$, </p>



[Go back to home page](/README.md)
