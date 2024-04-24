Comparison of FEM frameworks

# Simple tests

# 1. Simple advection (simple_advect_periodic_DG.py)

Advection of scalar field at unit velocity on a periodic domain $40 \times 10$ length units.  Advect left for $40$ time units.  Evaluates L2 error vs analytic profile at end of simulation.\
Mesh: $64 \times 16$ quadrilaterals, order-3 Lagrange polynomial basis functions.\
Time-stepper: RadauIIA order-2.\
Initial data: either Gaussian $n=e^{-\frac{r^2}{s^2}}$ or `Frankenstein's monster'-type curve $n=\mathrm{max}(0,e^{-\frac{a^2}{s^2-r^2}})$ (so-called as it's stitched onto zero with all derivatives continuous everywhere), both centered in the domain.

# 2. Slab anisotropic diffusion - Deluzet-Narski singular perturbation problem

Anisotropic diffusion problem in a square domain.  Contains anisotropy parameter $\eps < 1$; in the limit $\eps \rightarrow 0$ there is a null space (any function of $y$ satifying the Dirichlet BCs is in the solution space).

There are two numerical issues: the null space, and the `locking' problem.  The latter appears when the FEM basis functions lack a component which varies in the direction of the magnetic field - it is thus a problem at low order and goes away for higher-order.


