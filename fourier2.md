{% include mathjax.html %}

# Fourier Transform Visualization :

In the previous [page](/fourier.md) I introduced mathematically what Fourier Transforms are. Here I will build from that some visualizations that will help us construct an intuition of how Fourier Transforms work.

Let’s see some examples of the Fourier Transform of wavefunction (from position space to momentum space), keeping in mind the uncertainty principle. If the wavefunction in position space is well defined we should expect a flat wavefunction in momentum space and vise-versa. Consider a sinusoidal function in the position space given by $f(x)= \sin (2 \pi 250 x)$ with a wavelength of $\frac{1}{250} m$

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38459698-2694ba9a-3a7b-11e8-8cef-4bad82d5a505.jpg" width="500">
</p>

Then using the FFT function of Matlab, we obtain the Fourier Transform of the function in momentum domain as

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38653299-14975db0-3dd8-11e8-9e05-aa1f054df849.jpg" width="500">
</p>

As expected we see a peak at $\frac{k}{2\pi}=250 m^{-1}$ (notice that I used $\frac{k}{2\pi}$ not $k$ because $k= 2\pi \frac{1}{\lambda}$ and $\lambda = \frac{1}{250} m$). I also did the same for a function with two sin components $f(x)= \sin(2 \pi \cdot 250 \cdot t)+ \sin(2 \pi \cdot 150 \cdot t)$ and we can see the function in momentum domain with two peaks, one at each $k$ value:

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38653303-17b9d36a-3dd8-11e8-97fc-a00b6749e54a.jpg" width="500">
</p>
The fact that the Fourier Transform of a sinusoidal wave is a delta function should make sense. A sinusoidal function in the position domain means that the uncertainty of position value is very large, consequently, the uncertainty in momentum domain should be very small.

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

For high uncertainty in position:
<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38460807-8b2beb90-3a8f-11e8-98ef-756d82a8ebc2.jpg" width="300">
  <img src="https://user-images.githubusercontent.com/35305574/38460812-a1dd6b8e-3a8f-11e8-9d08-f576b3cf7c19.jpg" width="300">
</p>

For high less in position:
<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38460815-b3d30b8c-3a8f-11e8-875e-bd5717201a9c.jpg" width="300">
  <img src="https://user-images.githubusercontent.com/35305574/38460818-c0dc8f6a-3a8f-11e8-96b7-ba14aa9cb8aa.jpg" width="300">
</p>

For high lowest in position:
<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/38460820-ce5132ea-3a8f-11e8-8eb7-5ada0aceacb6.jpg" width="300">
  <img src="https://user-images.githubusercontent.com/35305574/38460822-da304f4c-3a8f-11e8-871d-3c8a37ff9caf.jpg" width="300">
</p>

The figures above show how decreasing the width of the Gaussian in position domain (meaning decreasing the uncertainty in position) increases the width of the Gaussian in momentum domain (increasing the uncertainty in momentum). 

Now with a better understanding of the position-momentum relation, let’s study a simulation of the time evolution of the values of position and momentum as follow. 

![Four1](/Untitled.gif) 

The figure above shows the evolution of the position (left) and momentum the momentum (right) in the comlex plane. The figure above shows the evolution of the position (left) and momentum the momentum (right) in the complex plane. The vertical planes show the x=o (red) and the k=0 (blue) points. First thing we can see from the figure is that as the position distribution becomes wider the momentum distribution becomes narrower, in agreement with what I have shown the figures above. Notice that when the momentum distribution is centered at $k=0$ the position function is always along the real (no imaginary part). The more the center of the momentum distribution goes way from the center, the kinkier the position distribution becomes. Similarly, the higher the position the kinkier the momentum is.





[Go back to home page](/README.md)
