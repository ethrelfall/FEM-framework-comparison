Comparison of FEM frameworks

# Simple tests

# 1. Simple advection (simple_advect_periodic_DG.py)

Advection of scalar field at unit velocity on a periodic domain $40 \times 10$ length units.  Advect left for $40$ time units.\
Mesh: $64 \times 16$ quadrilaterals, order-3 Lagrange polynomial basis functions.\
Time-stepper: RadauIIA order-2.\
Initial data: either Gaussian $n=e^{-\frac{r^2}{s^2}$ or `Frankenstein's monster'-type curve $n=e^{-\frac{a^2}{s^2-r^2}}$, both centered in the domain.


