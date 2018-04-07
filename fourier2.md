{% include mathjax.html %}

# Fourier Transform Visualization :

In the previous (page) I have introduced mathematically what is a Fourier Transform. Here I will build from that  some visualizations that will help build the intuition of how Fourier Transforms work.

Let’s see some examples of Fourier Transform of wavefunction from position space to momentum space, keeping in mind the uncertainty principle. If the wavefunction in position space is well defined we should expect a flat wavefunction in momentum space. If we consider a sinusoidal function in the position space $f(x)=sin(2 pi 250 t)$ with a frequency of $250 \frac{m}{s}$:

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38459698-2694ba9a-3a7b-11e8-8cef-4bad82d5a505.jpg" width="300">
</p>

Then using the FFT function of Matlab, we obtain the Fourier Transform of the function in momentum domain as

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38459731-88d192d2-3a7b-11e8-9f3d-62c7d3fcd495.jpg" width="300">
</p>

As expected we see a peak at $k=250 m^{-1}$. We can also do the for a function with two sin components $f(x)= sin(2pi\dot 250\dot t)+sin(2pi\dot 150\dot t)$ and we see the function in momentum domain with two peaks, one at each $k$ value:

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38459793-6a6d5b86-3a7c-11e8-869b-3cbf1b364562.jpg" width="300">
</p>
The fact that the Fourier Transform of a sinusoidal wave is a delta function should make sense. Since a sinusoidal function in the position domain means that the uncertainty of position value is very large, consequently, the uncertainty in momentum domain should be very small.

Let’s consider a function that would have minimal uncertainty in both position and momentum values. The type of function that satisfy this condition is the Gaussian function. The general form of a Gaussian is given by $f(x)= A e^{-c(x-b)^2}$, where $A$ scales the amplitude of the function, $c$ defines the linewidth and $b$ $ defines the center of the Gaussian.

In Matlab I create the Gaussian function using this code:
```Matlab
Psi_x=exp(-a*(x'-b).^2);

```
Then I compute the function in the momentum domain using the fft and fftshift shift finctions of matlab as follow:
```Matlab
psi_k = fft(psi_x);
psi_k = fftshift(psi_k);
```
Using this code I computed the Fourier transform of different Gaussian wavefunction that have different linewidths (higher uncertainty in the position) as shown in the figure bollow.

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38460807-8b2beb90-3a8f-11e8-98ef-756d82a8ebc2.jpg" width="300">
  <img src="https://user-images.githubusercontent.com/35305574/38460812-a1dd6b8e-3a8f-11e8-9d08-f576b3cf7c19.jpg" width="300">
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38460815-b3d30b8c-3a8f-11e8-875e-bd5717201a9c.jpg" width="300">
</p><p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38460818-c0dc8f6a-3a8f-11e8-96b7-ba14aa9cb8aa.jpg" width="300">
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38460820-ce5132ea-3a8f-11e8-8eb7-5ada0aceacb6.jpg" width="300">
</p><p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38460822-da304f4c-3a8f-11e8-871d-3c8a37ff9caf.jpg" width="300">
</p>


[Go back to home page](/README.md)
