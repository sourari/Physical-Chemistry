{% include mathjax.html %}


## Difference Method of Evaluating the TDSE

The difference method is a powerful tool of evaluating the TDSE, or any other differential equation. The benefit of this method is that it allows us to omit the need to evaluate the differential equation (or here the Schrödinger equation) for each time, instead it builds the state at each time () from the previous state (). Therefore, this method saves us a lot of computational power and simplifies the calculation significantly. However, these benefits come with a price. Building each state from the previous, means that each calculation will build on the error of the previous calculation, hence the error will exponentially increase. 
<p align="center"> $H \Psi(x,t)= i \hbar \frac{\partial}{\partial t} \Psi(x,t)$, </p>
Now let’s transition from the time differential to time difference $\Delta t$ so that 
<p align="center"> $H \Psi(x,t)= i \hbar \frac{\Delta \Psi(x,t)}{\Delta t} $, </p>




[Go back to home page](/README.md)
