{% include mathjax.html %}

# Fourier Transform Visualization :

In the previous (page) I have introduced mathematically what is a Fourier Transform. Here I will build from that  some visualizations that will help build the intuition of how Fourier Transforms work.

Let’s see some examples of Fourier Transform of wavefunction from position space to momentum space, keeping in mind the uncertainty principle. If the wavefunction in position space is well defined we should expect a flat wavefunction in momentum space. If we consider a sinusoidal function in the position space $f(x)=sin(2 pi 250 t)$ with a frequency of $250 \frac{m}{s}$:

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38459698-2694ba9a-3a7b-11e8-8cef-4bad82d5a505.jpg" width="500">
</p>

Then using the FFT function of Matlab, we obtain the Fourier Transform of the function in momentum domain as

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38459731-88d192d2-3a7b-11e8-9f3d-62c7d3fcd495.jpg" width="500">
</p>


<p align="center"> $\hat{f}(t)=\frac{1}{\sqrt[]{2\pi}}\int_{-\infty}^{\infty} f(\omega) e^{i\omega t}dx$. </p>



[Go back to home page](/README.md)
