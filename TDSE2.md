{% include mathjax.html %}

# Time Dependent Schroedinger Equation for the Particle in a Box System:

In this section we want to numerically solve the TDSE for the PIB using Matlab.
At this stage, we only want to have an overall idea of the behavior of a particle inside an infinit 2-D square potential. So, we will set all the constant to a value of $1$ in Matlab as follow

```Matlab
hbar=1;          %plank constant
me=1;            %mass electron
a=1;             %width of box
barrht=10^6;     %hight of barrier
pts=250;         %number of points discritizing space
barrier_width=3; %number of points with infinit potential

```
