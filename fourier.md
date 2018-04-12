{% include mathjax.html %}

# Fourier Transform:
So far in my analysis of quantum systems, I have been mainly using the position basis. However, there is a lot of information hidden in other bases, such as the momentum basis. Luckily for us, there is a powerful mathematical tool that can help us navigate easily between position and momentum bases. This mathematical tool is of course the glorious Fourier Transform. In this page, I will be introducing the basic math behind the Fourier transform and how it is helpful in physical chemistry.

The Fourier Transform decomposes a function into a sum of complex exponential function (or sinusoidal functions). Each of these functions has a different frequency and together they form a basis. The idea on Fourier Transform is to express our original function in this new basis (a familiar approach to what we discussed [here](/ChangeofBasis.md)).

Let’s explore the example of transforming a function from position space to momentum space. In momentum space, we use the wavenumber $k=\frac{2\pi}{\lambda}$ as our variable. To see why we use $k$ for the momentum space let’s apply the momentum operator on an arbitrary function $f(x)=e^{ikx}$ as follow

<p align="center"> $\hat{P}e^{ikx}= -i \hbar \frac{\partial}{\partial x}e^{ikx}$. </p>
so 
<p align="center"> $\hat{P}e^{ikx}= k \hbar e^{ikx}$. </p>
Therefore, the momentum eigenvalue is the wavenumber $k$ multiplied by $\hbar$. This is why we use $k$ as our variable in expressing the wavefunction in momentum space.

Now, I want to show how the Fourier Transform takes as an input a function in position space $f(x)$ and gives us a new function in $k$-space $\hat{f}(k)$ as an output. As we defined above, the Fourier Transform specifies how much a complex exponential function $e^{ikx}$ with wavenumber $k$ contributes to the function $f(x)$.  As we would expect, each $e^{ikx}$ will contribute to $f(x)$ by a coefficient that is dependent on the value of $k$. We define this coefficient by $\hat{f}(k)$. The function $f(x)$ is, therefore, the sum of all these contributions and can be written as
<p align="center"> $f(x)=\sum_{k} \hat{f}(k) e^{ikx}$. </p>

The expression above is for discrete values of $k$. To express $f(x)$ in function of continuous and infinite values of $k$, we have to change the sum into an integral as follow

<p align="center"> $f(x)=\frac{1}{\sqrt[]{2\pi}}\int_{-\infty}^{\infty} \hat{f}(k) e^{ikx}dk$. </p>

The above equation is known as the inverse Fourier Transform. The Fourier Transform is then given by
<p align="center"> $\hat{f}(k)=\frac{1}{\sqrt[]{2\pi}}\int_{-\infty}^{\infty} f(x) e^{-ikx}dx$. </p>


The same equations can be used to transform from the time domain to the frequency domain or vise-versa as follow
<p align="center"> $f(\omega)=\frac{1}{\sqrt[]{2\pi}}\int_{-\infty}^{\infty} \hat{f}(t) e^{-i\omega t}dt$. </p>
<p align="center"> $\hat{f}(t)=\frac{1}{\sqrt[]{2\pi}}\int_{-\infty}^{\infty} f(\omega) e^{i\omega t}d\omega$. </p>

The most important property of Fourier Transform is how they transform derivatives. Let’s consider the function $f(x)$ that has the property that $ {\lim}_{x\to \pm\infty}f(x) =0$. The Fourier Transform of the derivative of $f(x)$ is 

<p align="center"> $\mathscr{F}(\frac{d}{dx}f(x))=\mathscr{F}(f'(x))$ </p>
<p align="center"> $=\frac{1}{\sqrt[]{2\pi}}\int_{-\infty}^{\infty} f'(x) e^{-ikx}dx$. </p>

This integral can be solved using integration by part. Doing so, the Fourier Transform become 

<p align="center"> $ \frac{1}{\sqrt[]{2\pi}}[f(x)e^{-ikx}|_{-\infty}^{\infty} + ik\int_{-\infty}^{\infty} f(x) e^{-ikx}dx].$ </p>
But we know that $\lim_{x\to \pm\infty}f(x)=0$. Therefore, the first term in the equation above goes to zero and we obtain

<p align="center"> $ \mathscr{F}(\frac{d}{dx}f(x))= \frac{1}{\sqrt[]{2\pi}} (ik)\int_{-\infty}^{\infty} f(x) e^{-ikx}dx.$ </p>

Therefore, we can see that Fourier Transform converts the derivative to a multiplication by $ik$. Note that taking higher derivatives will result in higher factors of $ik$. This can be of a tremendous help in evaluating the Hamiltonian of complex systems. Since $\hat{H}=\hat{T} +\hat{V} $ and $\hat{T}$ is mainly a second derivative with respect to position, then it is beneficial to take the Fourier Transform of this operation and evaluate $\hat{T}$ in the momentum domain then recombine it with $\hat{V}$ (which is easier to leave in the position domain).

For a better understanding of how Fourier transform please visit my page on Fourier Transform visualization [here](/fourier2.md).


[Go back to home page](/README.md)
